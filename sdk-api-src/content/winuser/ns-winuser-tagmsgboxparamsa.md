---
UID: NS:winuser.tagMSGBOXPARAMSA
title: tagMSGBOXPARAMSA
author: windows-sdk-content
description: Contains information used to display a message box. The MessageBoxIndirect function uses this structure.
old-location: dlgbox\msgboxparams.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxstructures\msgboxparams.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*LPMSGBOXPARAMSA, *PMSGBOXPARAMSA, MSGBOXPARAMS, MSGBOXPARAMS structure [Dialog Boxes], MSGBOXPARAMSA, MSGBOXPARAMSW, PMSGBOXPARAMS, PMSGBOXPARAMS structure pointer [Dialog Boxes], _win32_MSGBOXPARAMS_str, _win32_msgboxparams_str_cpp, dlgbox.msgboxparams, tagMSGBOXPARAMSA, winui._win32_msgboxparams_str, winuser/MSGBOXPARAMS, winuser/MSGBOXPARAMSA, winuser/MSGBOXPARAMSW, winuser/PMSGBOXPARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MSGBOXPARAMSW (Unicode) and MSGBOXPARAMSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSGBOXPARAMSA, *PMSGBOXPARAMSA, *LPMSGBOXPARAMSA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winuser.h
api_name:
-	MSGBOXPARAMS
-	MSGBOXPARAMSA
-	MSGBOXPARAMSW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagMSGBOXPARAMSA structure


## -description


Contains information used to display a message box. The <a href="https://msdn.microsoft.com/3834bf46-0952-4e5c-bda4-6997576192d9">MessageBoxIndirect</a> function uses this structure.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The structure size, in bytes. 


### -field hwndOwner

Type: <b>HWND</b>

A handle to the owner window. This member can be <b>NULL</b>. 


### -field hInstance

Type: <b>HINSTANCE</b>

A handle to the module that contains the icon resource identified by the 
					<b>lpszIcon</b> member, and the string resource identified by the 
					<b>lpszText</b> or 
					<b>lpszCaption</b> member. 


### -field lpszText

Type: <b>LPCTSTR</b>

A null-terminated string, or the identifier of a string resource, that contains the message to be displayed. 


### -field lpszCaption

Type: <b>LPCTSTR</b>

A null-terminated string, or the identifier of a string resource, that contains the message box title. If this member is <b>NULL</b>, the default title 
					<b>Error</b> is used. 


### -field dwStyle

Type: <b>DWORD</b>

The contents and behavior of the dialog box. This member can be a combination of flags described for the 
					<i>uType</i> parameter of the <a href="https://msdn.microsoft.com/aca871a0-4767-4a7d-ab12-6eb7d03577ef">MessageBoxEx</a> function. 

In addition, you can specify the <b>MB_USERICON</b> flag (0x00000080L) if you want the message box to display the icon specified by the 
					<b>lpszIcon</b> member. 


### -field lpszIcon

Type: <b>LPCTSTR</b>

Identifies an icon resource. This parameter can be either a null-terminated string or an integer resource identifier passed to the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro. 

To load one of the standard system-defined icons, set the 
						<b>hInstance</b> member to <b>NULL</b> and set 
						<b>lpszIcon</b> to one of the values listed with the <a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a> function. 

This member is ignored if the 
						<b>dwStyle</b> member does not specify the <b>MB_USERICON</b> flag. 


### -field dwContextHelpId

Type: <b>DWORD_PTR</b>

Identifies a help context. If a help event occurs, this value is specified in the <a href="https://msdn.microsoft.com/8320fb68-294b-487b-ab5a-6611bb57cff0">HELPINFO</a> structure that the message box sends to the owner window or callback function. 


### -field lpfnMsgBoxCallback

Type: <b>MSGBOXCALLBACK</b>

A pointer to the callback function that processes help events for the message box. The callback function has the following form:
		

<code>VOID CALLBACK MsgBoxCallback(LPHELPINFO lpHelpInfo);</code>

If this member is <b>NULL</b>, the message box sends 
					<a href="https://msdn.microsoft.com/6a090125-67dd-4267-9973-10e32c6e4f1f">WM_HELP</a> messages to the owner window when help events occur. 


### -field dwLanguageId

Type: <b>DWORD</b>

The language in which to display the text contained in the predefined push buttons. This value must be in the form returned by the 
					<a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a> macro. 

For a list of supported language identifiers, see <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">Language Identifiers</a>. Note that each localized release of Windows typically contains resources only for a limited set of languages. Thus, for example, the U.S. version offers <b>LANG_ENGLISH</b>, the French version offers <b>LANG_FRENCH</b>, the German version offers <b>LANG_GERMAN</b>, and the Japanese version offers <b>LANG_JAPANESE</b>. Each version offers <b>LANG_NEUTRAL</b>. This limits the set of values that can be used with the 
					<b>dwLanguageId</b> parameter. Before specifying a language identifier, you should enumerate the locales that are installed on a system. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/8320fb68-294b-487b-ab5a-6611bb57cff0">HELPINFO</a>



<a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>



<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<a href="https://msdn.microsoft.com/cdf6424a-bf2b-4c14-8bc7-8b5f04c29ed3">MAKELANGID</a>



<a href="https://msdn.microsoft.com/aca871a0-4767-4a7d-ab12-6eb7d03577ef">MessageBoxEx</a>



<a href="https://msdn.microsoft.com/3834bf46-0952-4e5c-bda4-6997576192d9">MessageBoxIndirect</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/6a090125-67dd-4267-9973-10e32c6e4f1f">WM_HELP</a>
 

 

