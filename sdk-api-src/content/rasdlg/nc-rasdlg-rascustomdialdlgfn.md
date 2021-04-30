---
UID: NC:rasdlg.RasCustomDialDlgFn
title: RasCustomDialDlgFn (rasdlg.h)
description: The RasCustomDialDlg function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom RAS connection dialog boxes.
helpviewer_keywords: ["RCD_Logon","RasCustomDialDlg","RasCustomDialDlg callback function [RAS]","RasCustomDialDlgA","RasCustomDialDlgFn","RasCustomDialDlgFn callback","RasCustomDialDlgW","_ras_rascustomdialdlg","rasdlg/RasCustomDialDlg","rasdlg/RasCustomDialDlgA","rasdlg/RasCustomDialDlgW","rras.rascustomdialdlg"]
old-location: rras\rascustomdialdlg.htm
tech.root: RRAS
ms.assetid: d1f4715a-a31c-4346-ac0a-83f2c58e8cc1
ms.date: 12/05/2018
ms.keywords: RCD_Logon, RasCustomDialDlg, RasCustomDialDlg callback function [RAS], RasCustomDialDlgA, RasCustomDialDlgFn, RasCustomDialDlgFn callback, RasCustomDialDlgW, _ras_rascustomdialdlg, rasdlg/RasCustomDialDlg, rasdlg/RasCustomDialDlgA, rasdlg/RasCustomDialDlgW, rras.rascustomdialdlg
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasCustomDialDlgFn
 - rasdlg/RasCustomDialDlgFn
dev_langs:
 - c++
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
If this flag is set to one, the connection was dialed from a Windows Logon context. <a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> uses this information to get the appropriate user preferences for the connection entry. If <b>RasDial</b> is called from this entry point, the <i>dwfOptions</i> member of the <i>lpRasDialExtension</i> parameter must have the <b>RDEOPT_NoUser</b> flag set to indicate the connection was dialed from a Windows Logon context.

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
<a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga">RasDialDlg</a> uses the numbers in the phone-book entry.

### -param lpInfo

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)">RASDIALDLG</a> structure that contains additional input and output parameters. On input, the <b>dwSize</b> member of this structure must specify sizeof(
<b>RASDIALDLG</b>). If an error occurs, the <b>dwError</b> member returns an error code; otherwise, it returns zero.

### -param pvInfo

Reserved for internal use. This parameter will always be <b>NULL</b>.

## -returns

If the user creates, copies, or edits a phone-book entry, the return value should be <b>TRUE</b>. Otherwise, the function should return <b>FALSE</b>.

If an error occurs, 
<a href="/windows/desktop/api/rasdlg/nc-rasdlg-rascustomentrydlgfn">RasCustomEntryDlg</a> should set the <b>dwError</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)">RASENTRYDLG</a> structure to a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

## -remarks

RAS calls this entry point from 
<a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga">RasDialDlg</a>, if the <b>szCustomDialDll</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure for the entry being dialed specifies a custom-dialing DLL.

If this entry point calls 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>, the <i>lpRasDialExtensions</i> parameter must not be <b>NULL</b>, and the <b>dwfOptions</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)">RASDIALEXTENSIONS</a> structure must have the <b>RDEOPT_CustomDial</b> flag set.

The custom-dial dialog must support 
<a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> messages where 
<a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a>(<i>wParam</i>) equals IDCANCEL.

If the custom-dial DLL does not support this entry point, RAS returns <b>ERROR_CANNOT_DO_CUSTOMDIAL</b> to the caller of 
<a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga">RasDialDlg</a>.

## -see-also

<a href="/windows/desktop/RRAS/custom-dialers">Custom Dialers</a>



<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomdialfn">RasCustomDial</a>



<a href="/windows/desktop/api/rasdlg/nc-rasdlg-rascustomentrydlgfn">RasCustomEntryDlg</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomhangupfn">RasCustomHangUp</a>



<a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga">RasDialDlg</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>