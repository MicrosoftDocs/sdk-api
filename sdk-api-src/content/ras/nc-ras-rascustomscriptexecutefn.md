---
UID: NC:ras.RasCustomScriptExecuteFn
title: RasCustomScriptExecuteFn (ras.h)
description: RAS calls the RasCustomScriptExecute function when establishing a connection for a phone-book entry that has the RASEO_CustomScript option set.
helpviewer_keywords: ["RasCustomScriptExecute","RasCustomScriptExecute callback function [RAS]","RasCustomScriptExecuteFn","RasCustomScriptExecuteFn callback","_ras_rascustomscriptexecute","ras/RasCustomScriptExecute","rras.rascustomscriptexecute"]
old-location: rras\rascustomscriptexecute.htm
tech.root: RRAS
ms.assetid: e31ab530-cb60-4bb0-be44-3ba90fdf71f1
ms.date: 12/05/2018
ms.keywords: RasCustomScriptExecute, RasCustomScriptExecute callback function [RAS], RasCustomScriptExecuteFn, RasCustomScriptExecuteFn callback, _ras_rascustomscriptexecute, ras/RasCustomScriptExecute, rras.rascustomscriptexecute
req.header: ras.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasCustomScriptExecuteFn
 - ras/RasCustomScriptExecuteFn
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
 - RasCustomScriptExecute
---

# RasCustomScriptExecuteFn callback function


## -description

RAS calls the 
<b>RasCustomScriptExecute</b> function when establishing a connection for a phone-book entry that has the 
<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASEO_CustomScript</a> option set.

## -parameters

### -param hPort [in]

Handle to the port on which the connection is established. Use this handle when sending or receiving data on the port.

### -param lpszPhonebook [in]

Pointer to a Unicode string that contains the path to the phone book in which the entry for the connection resides.

### -param lpszEntryName [in]

Pointer to a Unicode string that contains the name of the entry that was dialed to establish the connection.

### -param pfnRasGetBuffer [in]

Pointer to a function of type 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasgetbuffer">PFNRASGETBUFFER</a>. The custom-scripting DLL should use this function to allocate memory to send data to the server.

### -param pfnRasFreeBuffer [in]

Pointer to a function of type 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasfreebuffer">PFNRASFREEBUFFER</a>. The custom-scripting DLL should use this function to free memory allocated by the 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasgetbuffer">pfnRasGetBuffer</a> function.

### -param pfnRasSendBuffer [in]

Pointer to a function of type 
<a href="/windows/desktop/api/ras/nc-ras-pfnrassendbuffer">PFNRASSENDBUFFER</a>. The custom-scripting DLL uses this function to communicate with the server over the specified port.

### -param pfnRasReceiveBuffer [in]

Pointer to a function of type 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasreceivebuffer">PFNRASRECEIVEBUFFER</a>. The custom-scripting DLL uses this function to communicate with the server over the specified port.

### -param pfnRasRetrieveBuffer [in]

Pointer to a function of type 
<a href="/windows/desktop/api/ras/nc-ras-pfnrasretrievebuffer">PFNRASRETRIEVEBUFFER</a>. The custom-scripting DLL uses this function to communicate with the server over the specified port.

### -param hWnd [in]

Handle to a window that the custom-scripting DLL can use to present a user interface to the user.

### -param pRasDialParams [in]

Pointer to a Unicode 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> structure. This structure contains the authentication credentials for the user. The custom-scripting DLL can modify the <b>szUserName</b>, <b>szPassword</b>, and <b>szDomain</b> members of this structure. The Point-to-Point Protocol (PPP) will use whatever is stored in these members when 
<b>RasCustomScriptExecute</b> returns.

### -param pvReserved

#### - pRasCustomScriptExtensions [in]

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)">RASCUSTOMSCRIPTEXTENSIONS</a> structure. This structure contains pointers to additional functions for the custom-scripting DLL.

<b>Windows 2000:  </b>This parameter is supported on Windows SP2 and later.

## -returns

If the function succeeds, the return value should be <b>ERROR_SUCCESS</b>.

If the function fails, the return value should be an appropriate error code from Winerror.h or Raserror.h.

## -remarks

When RAS calls 
<b>RasCustomScriptExecute</b>, the <i>pRasDialParams</i> parameter will point to the Unicode 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> structure. That is, the structure contains only Unicode strings.

In some cases, the <b>szUserName</b> of the 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> structure will be an empty string. In these cases, the custom-scripting DLL should use the Unicode version of the 
<a href="/windows/desktop/DirectShow/iamtimelineobj-getusername">GetUserName</a> function to obtain the name of the current user.

## -see-also

<a href="/windows/desktop/RRAS/ras-custom-scripting">RAS Custom-Scripting</a>



<a href="/windows/desktop/api/ras/nc-ras-pfnrasfreebuffer">RasFreeBuffer</a>



<a href="/windows/desktop/api/ras/nc-ras-pfnrasgetbuffer">RasGetBuffer</a>



<a href="/windows/desktop/api/ras/nc-ras-pfnrasreceivebuffer">RasReceiveBuffer</a>



<a href="/windows/desktop/api/ras/nc-ras-pfnrasretrievebuffer">RasRetrieveBuffer</a>



<a href="/windows/desktop/api/ras/nc-ras-pfnrassendbuffer">RasSendBuffer</a>
