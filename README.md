# Return-SetError
   Switch $iPoint         Case -1             ; No change         Case Default             $aMarquee_Params[$iIndex][10] = $aMarquee_Params[0][10]         Case Else             If IsNumber($iPoint) Then                 $aMarquee_Params[$iIndex][10] = Int(Abs($iPoint / .75))             Else                 Return SetError(1, 5, 0)             EndIf     EndSwitch      Switch $sFont         Case ""             ; No change         Case Default             $aMarquee_Params[$iIndex][11] = $aMarquee_Params[0][11]         Case Else             If IsString($sFont) Then                 $aMarquee_Params[$iIndex][11] = $sFont             Else                 Return SetError(1, 5, 0)             EndIf     EndSwitch      Return 1  EndFunc   ;==>_GUICtrlMarquee_SetDisplay
