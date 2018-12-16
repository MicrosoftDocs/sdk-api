---
UID: NF:tapi.lineTranslateDialog
title: lineTranslateDialog function
author: windows-sdk-content
description: The lineTranslateDialog function displays an application-modal dialog box that allows the user to change the current location of a phone number about to be dialed, adjust location and calling card parameters, and see the effect.
old-location: tapi2\linetranslatedialog.htm
tech.root: tapi
ms.assetid: c9fd7abb-3b4b-442b-badc-371a12724f67
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linetranslatedialog, lineTranslateDialog, lineTranslateDialog function [TAPI 2.2], lineTranslateDialogA, lineTranslateDialogW, tapi/lineTranslateDialog, tapi/lineTranslateDialogA, tapi/lineTranslateDialogW, tapi2.linetranslatedialog"
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineTranslateDialogW (Unicode) and lineTranslateDialogA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineTranslateDialog
 - lineTranslateDialogA
 - lineTranslateDialogW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineTranslateDialog function


## -description


The 
<b>lineTranslateDialog</b> function displays an application-modal dialog box that allows the user to change the current location of a phone number about to be dialed, adjust location and calling card parameters, and see the effect.


## -parameters




### -param hLineApp

Application handle returned by 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>. If an application has not yet called the 
<b>lineInitializeEx</b> function, it can set the <i>hLineApp</i> parameter to zero.


### -param dwDeviceID

Device identifier for the line device upon which the call is intended to be dialed, so that variations in dialing procedures on different lines can be applied to the translation process.


### -param dwAPIVersion

Highest version of TAPI supported by the application (not necessarily the value negotiated by 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a> on the line device indicated by <i>dwDeviceID</i>).


### -param hwndOwner

Handle to a window to which the dialog box is to be attached. Can be a <b>NULL</b> value to indicate that any window created during the function should have no owner window.


### -param lpszAddressIn

Pointer to a <b>null</b>-terminated string containing a phone number that is used, in the lower portion of the dialog box, to show the effect of the user's changes on the location parameters. The number must be in canonical format; if noncanonical, the phone number portion of the dialog box is not displayed. This pointer can be left <b>NULL</b>, in which case the phone number portion of the dialog box is not displayed. If the <i>lpszAddressIn</i> parameter contains a subaddress or name field, or additional addresses separated from the first address by CR and LF characters, only the first address is used in the dialog box.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_INVALPARAM, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_INVALPOINTER, LINEERR_INIFILECORRUPT, LINEERR_NODRIVER, LINEERR_INUSE, LINEERR_NOMEM, LINEERR_INVALADDRESS, LINEERR_INVALAPPHANDLE, LINEERR_OPERATIONFAILED.




## -remarks



In TAPI version 2.0 or later, it is possible for multiple instances of this dialog box to be opened. In TAPI versions earlier than 2.0, LINEERR_INUSE is returned if the dialog box is already displayed by another application (it cannot be open more than once). In these versions, TAPI brings the existing dialog box to the front, and the error indicates that any particulars related to the address passed in by the current application have not been handled, because that address was not processed by the function.

The application must call 
<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a> after this function to obtain any changes the user made to the telephony address translation parameters, and call 
<a href="https://msdn.microsoft.com/0347d526-9596-4b42-8075-07318bf39634">lineTranslateAddress</a> to obtain a dialable string based on the user's new selections.

If any function related to address translation (for example, 
<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a> or 
<a href="https://msdn.microsoft.com/0347d526-9596-4b42-8075-07318bf39634">lineTranslateAddress</a>) returns LINEERR_INIFILECORRUPT, the application should call 
<b>lineTranslateDialog</b>. The 
<b>lineTranslateDialog</b> function detects the errors and corrects them, and reports the action taken to the user.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>



<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>



<a href="https://msdn.microsoft.com/0347d526-9596-4b42-8075-07318bf39634">lineTranslateAddress</a>
 

 

