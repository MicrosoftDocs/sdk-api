---
UID: NC:rasdlg.RasCustomDialDlgFn
title: RasCustomDialDlgFn
author: windows-sdk-content
description: The RasCustomDialDlg function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom RAS connection dialog boxes.
old-location: rras\rascustomdialdlg.htm
tech.root: rras
ms.assetid: d1f4715a-a31c-4346-ac0a-83f2c58e8cc1
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: RCD_Logon, RasCustomDialDlg, RasCustomDialDlg callback function [RAS], RasCustomDialDlgA, RasCustomDialDlgFn, RasCustomDialDlgFn callback, RasCustomDialDlgW, _ras_rascustomdialdlg, rasdlg/RasCustomDialDlg, rasdlg/RasCustomDialDlgA, rasdlg/RasCustomDialDlgW, rras.rascustomdialdlg
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: rasdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasCustomDialDlgW (Unicode) and RasCustomDialDlgA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Rasdlg.h
api_name:
 - RasCustomDialDlg
 - RasCustomDialDlgA
 - RasCustomDialDlgW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasCustomDialDlgFn callback function


## -description


<p class="CCE_Message">[This function is not available as of Windows Server 2008.

]

The 
<b>RasCustomDialDlg</b> function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom RAS connection dialog boxes.


## -parameters




### -param hInstDll

Handle to the instance of the custom-dialing DLL that was loaded.


### -param dwFlags

A set of bit flags that specify <b>RasCustomDialDlg</b> options. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RCD_Logon"></a><a id="rcd_logon"></a><a id="RCD_LOGON"></a><dl>
<dt><b>RCD_Logon</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set to one, the connection was dialed from a Windows Logon context. <a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> uses this information to get the appropriate user preferences for the connection entry. If <b>RasDial</b> is called from this entry point, the <i>dwfOptions</i> member of the <i>lpRasDialExtension</i> parameter must have the <b>RDEOPT_NoUser</b> flag set to indicate the connection was dialed from a Windows Logon context.

</td>
</tr>
</table>
 

<b>Windows Server 2003 and Windows XP/2000:  </b>This parameter is reserved and should not be used.


### -param lpszPhonebook

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.


### -param lpszEntry

Pointer to a <b>null</b>-terminated string that contains the name of the phone-book entry to dial.


### -param lpszPhoneNumber

Pointer to a <b>null</b>-terminated string that contains a phone number that overrides the numbers stored in the phone-book entry. If this parameter is <b>NULL</b>, 
<a href="https://msdn.microsoft.com/698a18a1-b302-4b0d-8399-0bbdbe775f08">RasDialDlg</a> uses the numbers in the phone-book entry.


### -param lpInfo

Pointer to a 
<a href="https://msdn.microsoft.com/7a529aa6-3a75-44b8-bae3-0edc5c653825">RASDIALDLG</a> structure that contains additional input and output parameters. On input, the <b>dwSize</b> member of this structure must specify sizeof(
<b>RASDIALDLG</b>). If an error occurs, the <b>dwError</b> member returns an error code; otherwise, it returns zero.


### -param pvInfo

Reserved for internal use. This parameter will always be <b>NULL</b>.


## -returns



If the user creates, copies, or edits a phone-book entry, the return value should be <b>TRUE</b>. Otherwise, the function should return <b>FALSE</b>.

If an error occurs, 
<a href="https://msdn.microsoft.com/4778069b-87d0-4379-95f7-718fe0d7a56c">RasCustomEntryDlg</a> should set the <b>dwError</b> member of the 
<a href="https://msdn.microsoft.com/b7f3cd3f-3d16-407e-b17b-488ce2b00d43">RASENTRYDLG</a> structure to a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.




## -remarks



RAS calls this entry point from 
<a href="https://msdn.microsoft.com/698a18a1-b302-4b0d-8399-0bbdbe775f08">RasDialDlg</a>, if the <b>szCustomDialDll</b> member of the 
<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a> structure for the entry being dialed specifies a custom-dialing DLL.

If this entry point calls 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>, the <i>lpRasDialExtensions</i> parameter must not be <b>NULL</b>, and the <b>dwfOptions</b> member of the 
<a href="https://msdn.microsoft.com/533c9ab4-69d0-492d-81c6-2c07ca219fc7">RASDIALEXTENSIONS</a> structure must have the <b>RDEOPT_CustomDial</b> flag set.

The custom-dial dialog must support 
<a href="_win32_wm_command">WM_COMMAND</a> messages where 
<a href="_win32_loword">LOWORD</a>(<i>wParam</i>) equals IDCANCEL.

If the custom-dial DLL does not support this entry point, RAS returns <b>ERROR_CANNOT_DO_CUSTOMDIAL</b> to the caller of 
<a href="https://msdn.microsoft.com/698a18a1-b302-4b0d-8399-0bbdbe775f08">RasDialDlg</a>.




## -see-also




<a href="https://msdn.microsoft.com/ad94f38d-812f-4329-8055-6274a21a3242">Custom Dialers</a>



<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a>



<a href="https://msdn.microsoft.com/8c3f807b-3e31-4ce6-8549-74ab06cbba7f">RasCustomDial</a>



<a href="https://msdn.microsoft.com/4778069b-87d0-4379-95f7-718fe0d7a56c">RasCustomEntryDlg</a>



<a href="https://msdn.microsoft.com/56410af3-7b23-4536-998d-88d78d45585d">RasCustomHangUp</a>



<a href="https://msdn.microsoft.com/698a18a1-b302-4b0d-8399-0bbdbe775f08">RasDialDlg</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

