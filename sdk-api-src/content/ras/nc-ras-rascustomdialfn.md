---
UID: NC:ras.RasCustomDialFn
title: RasCustomDialFn (ras.h)
description: The RasCustomDial function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom remote-access dialing routines.
helpviewer_keywords: ["RasCustomDial","RasCustomDial callback function [RAS]","RasCustomDialA","RasCustomDialFn","RasCustomDialFn callback","RasCustomDialW","_ras_rascustomdial","ras/RasCustomDial","ras/RasCustomDialA","ras/RasCustomDialW","rras.rascustomdial"]
old-location: rras\rascustomdial.htm
tech.root: RRAS
ms.assetid: 8c3f807b-3e31-4ce6-8549-74ab06cbba7f
ms.date: 12/05/2018
ms.keywords: RasCustomDial, RasCustomDial callback function [RAS], RasCustomDialA, RasCustomDialFn, RasCustomDialFn callback, RasCustomDialW, _ras_rascustomdial, ras/RasCustomDial, ras/RasCustomDialA, ras/RasCustomDialW, rras.rascustomdial
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasCustomDialW (Unicode) and RasCustomDialA (ANSI)
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
 - RasCustomDialFn
 - ras/RasCustomDialFn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RasCustomDial
 - RasCustomDialA
 - RasCustomDialW
---

# RasCustomDialFn callback function


## -description

<p class="CCE_Message">[This function is not available as of Windows Server 2008.

]

The 
<b>RasCustomDial</b> function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom remote-access dialing routines.

## -parameters

### -param hInstDll

Handle to the instance of the custom-dial DLL that was loaded.

### -param lpRasDialExtensions

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)">RASDIALEXTENSIONS</a> structure that specifies a set of 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> extended features to enable. Set this parameter to <b>NULL</b> if there is no need to enable the extensions.

### -param lpszPhonebook

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.

### -param lpRasDialParams

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> structure that specifies calling parameters for the RAS connection. 




The caller must set the 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> structure's <b>dwSize</b> member to sizeof(<b>RASDIALPARAMS</b>) to identify the version of the structure being passed.

### -param dwNotifierType

This parameter is the same as the <i>dwNotifierType</i> parameter for the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function. See the 
<b>RasDial</b> reference page for more information.

### -param lpvNotifier

This parameter is the same as the <i>lpvNotifier</i> parameter for the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function. See the 
<b>RasDial</b> reference page for more information.

### -param lphRasConn

Pointer to a variable of type <b>HRASCONN</b>. Set the <b>HRASCONN</b> variable to <b>NULL</b> before calling 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>. If 
<b>RasDial</b> succeeds, it stores a handle to the RAS connection into <i>*lphRasConn</i>.

### -param dwFlags

This parameter reserved for future use.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and a handle to the RAS connection in the variable pointed to by the <i>lphRasConn</i> parameter is returned.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function could not allocate sufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

RAS calls this entry point from 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>, if the <b>szCustomDialDll</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure for the entry being dialed specifies a custom-dialing DLL.

If this entry point calls 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>, the <i>lpRasDialExtensions</i> parameter must not be <b>NULL</b>, and the <b>dwFlags</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)">RASDIALEXTENSIONS</a> structure must have the RDEOPT_CustomDial flag set.

If the custom-dial DLL does not support this entry point, RAS returns ERROR_CANNOT_DO_CUSTOMDIAL to the caller of 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>.

## -see-also

<a href="/windows/desktop/RRAS/custom-dialers">Custom Dialers</a>



<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a>



<a href="/windows/desktop/api/rasdlg/nc-rasdlg-rascustomdialdlgfn">RasCustomDialDlg</a>



<a href="/windows/desktop/api/rasdlg/nc-rasdlg-rascustomentrydlgfn">RasCustomEntryDlg</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomhangupfn">RasCustomHangUp</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>