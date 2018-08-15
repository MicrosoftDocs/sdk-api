---
UID: NC:rasdlg.RasCustomEntryDlgFn
title: RasCustomEntryDlgFn
author: windows-sdk-content
description: The RasCustomEntryDlg function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom dialogs for managing phone-book entries.
old-location: rras\rascustomentrydlg.htm
old-project: rras
ms.assetid: 4778069b-87d0-4379-95f7-718fe0d7a56c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RasCustomEntryDlg, RasCustomEntryDlg callback function [RAS], RasCustomEntryDlgFn, RasCustomEntryDlgFn callback, _ras_rascustomentrydlg, rasdlg/RasCustomEntryDlg, rras.rascustomentrydlg
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: rasdlg.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RASNAPSTATE, *LPRASNAPSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Rasdlg.h
api_name:
 - RasCustomEntryDlg
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# RasCustomEntryDlgFn callback function


## -description


The 
<b>RasCustomEntryDlg</b> function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom dialogs for managing phone-book entries.


## -parameters




### -param hInstDll

Handle to the instance of the custom-dial DLL that was loaded.


### -param lpszPhonebook

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.


### -param lpszEntry

Pointer to a <b>null</b>-terminated string that contains the name of the phone-book entry to edit, copy, or create. 




If you are editing or copying an entry, this parameter is the name of an existing phone-book entry. If you are copying an entry, set the RASEDFLAG_CloneEntry flag in the <b>dwFlags</b> member of the 
<a href="https://msdn.microsoft.com/b7f3cd3f-3d16-407e-b17b-488ce2b00d43">RASENTRYDLG</a> structure.

If you are creating an entry, this parameter is a default new entry name that the user can change. If this parameter is <b>NULL</b>, the function provides a default name. If you are creating an entry, set the RASEDFLAG_NewEntry flag in the <b>dwFlags</b> member of the 
<a href="https://msdn.microsoft.com/b7f3cd3f-3d16-407e-b17b-488ce2b00d43">RASENTRYDLG</a> structure.


### -param lpInfo

Pointer to a 
<a href="https://msdn.microsoft.com/b7f3cd3f-3d16-407e-b17b-488ce2b00d43">RASENTRYDLG</a> structure that contains additional input and output parameters. On input, the <b>dwSize</b> member of this structure must specify sizeof(
<b>RASENTRYDLG</b>). Use the <b>dwSize</b> member to indicate whether creating, editing, or copying an entry. If an error occurs, the <b>dwError</b> member returns an error code; otherwise, it returns zero.


### -param dwFlags

Reserved for future use.


## -returns



If the user creates, copies, or edits a phone-book entry, the return value should be <b>TRUE</b>. Otherwise, the function should return <b>FALSE</b>.

If an error occurs, <b>RasCustomEntryDlg</b> should set the <b>dwError</b> member of the 
<a href="https://msdn.microsoft.com/b7f3cd3f-3d16-407e-b17b-488ce2b00d43">RASENTRYDLG</a> structure to a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.




## -remarks



RAS  calls this entry point from 
<a href="https://msdn.microsoft.com/9259502d-c31b-4ebd-ace7-70f02bbb7873">RasEntryDlg</a>, if the <b>szCustomDialDll</b> member of the 
<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a> structure for the entry being dialed specifies a custom-dialing DLL.

If the custom-dial DLL does not support this entry point, RAS returns ERROR_NO_CUSTOMENTRYDLG to the caller of 
<a href="https://msdn.microsoft.com/9259502d-c31b-4ebd-ace7-70f02bbb7873">RasEntryDlg</a>.




## -see-also




<a href="https://msdn.microsoft.com/ad94f38d-812f-4329-8055-6274a21a3242">Custom Dialers</a>



<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a>



<a href="https://msdn.microsoft.com/8c3f807b-3e31-4ce6-8549-74ab06cbba7f">RasCustomDial</a>



<a href="https://msdn.microsoft.com/d1f4715a-a31c-4346-ac0a-83f2c58e8cc1">RasCustomDialDlg</a>



<a href="https://msdn.microsoft.com/56410af3-7b23-4536-998d-88d78d45585d">RasCustomHangUp</a>



<a href="https://msdn.microsoft.com/9259502d-c31b-4ebd-ace7-70f02bbb7873">RasEntryDlg</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

