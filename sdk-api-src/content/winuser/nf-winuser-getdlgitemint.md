---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetDlgItemInt function


## -description


Translates the text of a specified control in a dialog box into an integer value. 


## -parameters




### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box that contains the control of interest. 


### -param nIDDlgItem [in]

Type: <b>int</b>

The identifier of the control whose text is to be translated. 


### -param lpTranslated [out, optional]

Type: <b>BOOL*</b>

Indicates success or failure (<b>TRUE</b> indicates success, <b>FALSE</b> indicates failure). 

If this parameter is <b>NULL</b>, the function returns no information about success or failure.


### -param bSigned [in]

Type: <b>BOOL</b>

Indicates whether the function should examine the text for a minus sign at the beginning and return a signed integer value if it finds one (<b>TRUE</b> specifies this should be done, <b>FALSE</b> that it should not). 


## -returns



Type: <b>UINT</b>

If the function succeeds, the variable pointed to by <i>lpTranslated</i> is set to <b>TRUE</b>, and the return value is the translated value of the control text. 

If the function fails, the variable pointed to by <i>lpTranslated</i> is set to <b>FALSE</b>, and the return value is zero. Note that, because zero is a possible translated value, a return value of zero does not by itself indicate failure.

If <i>lpTranslated</i> is <b>NULL</b>, the function returns no information about success or failure.

Note that, if the <i>bSigned</i> parameter is <b>TRUE</b> and there is a minus sign (–) at the beginning of the text, <b>GetDlgItemInt</b> translates the text into a signed integer value. Otherwise, the function creates an unsigned integer value. To obtain the proper value in this case, cast the return value to an <b>int</b> type.

To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>GetDlgItemInt</b> function retrieves the text of the specified control by sending the control a <a href="https://msdn.microsoft.com/117c3d6d-24cd-462f-bdb0-b65d8914273a">WM_GETTEXT</a> message. The function translates the retrieved text by stripping any extra spaces at the beginning of the text and then converting the decimal digits. The function stops translating when it reaches the end of the text or encounters a nonnumeric character. 

The <b>GetDlgItemInt</b> function returns zero if the translated value is greater than <b>INT_MAX</b> (for signed numbers) or <b>UINT_MAX</b> (for unsigned numbers). 


#### Examples


			
			For an example, see <a href="using_dialog_boxes.htm">Creating a Modeless Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/25ad5328-a91f-438b-9333-e49167b27b13">GetDlgCtrlID</a>



<a href="https://msdn.microsoft.com/c119d716-b07f-4644-9d51-da94fab3e516">GetDlgItem</a>



<a href="https://msdn.microsoft.com/6cfaa693-aafe-4034-abcb-0a8364cccb4b">GetDlgItemText</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8c71aa0e-1287-4a56-bef5-bcdddc9d9332">SetDlgItemInt</a>
 

 

