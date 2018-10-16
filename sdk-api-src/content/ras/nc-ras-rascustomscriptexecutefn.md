---
UID: NC:ras.RasCustomScriptExecuteFn
title: RasCustomScriptExecuteFn
author: windows-sdk-content
description: RAS calls the RasCustomScriptExecute function when establishing a connection for a phone-book entry that has the RASEO_CustomScript option set.
old-location: rras\rascustomscriptexecute.htm
tech.root: rras
ms.assetid: e31ab530-cb60-4bb0-be44-3ba90fdf71f1
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: RasCustomScriptExecute, RasCustomScriptExecute callback function [RAS], RasCustomScriptExecuteFn, RasCustomScriptExecuteFn callback, _ras_rascustomscriptexecute, ras/RasCustomScriptExecute, rras.rascustomscriptexecute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RasCustomScriptExecute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasCustomScriptExecuteFn callback function


## -description


RAS calls the 
<b>RasCustomScriptExecute</b> function when establishing a connection for a phone-book entry that has the 
<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASEO_CustomScript</a> option set.


## -parameters




### -param hPort [in]

Handle to the port on which the connection is established. Use this handle when sending or receiving data on the port.


### -param lpszPhonebook [in]

Pointer to a Unicode string that contains the path to the phone book in which the entry for the connection resides.


### -param lpszEntryName [in]

Pointer to a Unicode string that contains the name of the entry that was dialed to establish the connection.


### -param pfnRasGetBuffer [in]

Pointer to a function of type 
<a href="https://msdn.microsoft.com/655f2dfa-a6cf-43db-8d2e-bf9a10163c75">PFNRASGETBUFFER</a>. The custom-scripting DLL should use this function to allocate memory to send data to the server.


### -param pfnRasFreeBuffer [in]

Pointer to a function of type 
<a href="https://msdn.microsoft.com/aba43ef9-7f62-48ab-a790-c8592a57f2c2">PFNRASFREEBUFFER</a>. The custom-scripting DLL should use this function to free memory allocated by the 
<a href="https://msdn.microsoft.com/655f2dfa-a6cf-43db-8d2e-bf9a10163c75">pfnRasGetBuffer</a> function.


### -param pfnRasSendBuffer [in]

Pointer to a function of type 
<a href="https://msdn.microsoft.com/157a2bc7-351f-4170-b85b-ed789b4997ab">PFNRASSENDBUFFER</a>. The custom-scripting DLL uses this function to communicate with the server over the specified port.


### -param pfnRasReceiveBuffer [in]

Pointer to a function of type 
<a href="https://msdn.microsoft.com/cc5523df-748d-4f96-8d54-bf0a2f9ecde4">PFNRASRECEIVEBUFFER</a>. The custom-scripting DLL uses this function to communicate with the server over the specified port.


### -param pfnRasRetrieveBuffer [in]

Pointer to a function of type 
<a href="https://msdn.microsoft.com/5dc8a034-f1cb-47c5-8d60-06f314a85f11">PFNRASRETRIEVEBUFFER</a>. The custom-scripting DLL uses this function to communicate with the server over the specified port.


### -param hWnd [in]

Handle to a window that the custom-scripting DLL can use to present a user interface to the user.


### -param *pRasDialParams [in]

Pointer to a Unicode 
<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> structure. This structure contains the authentication credentials for the user. The custom-scripting DLL can modify the <b>szUserName</b>, <b>szPassword</b>, and <b>szDomain</b> members of this structure. The Point-to-Point Protocol (PPP) will use whatever is stored in these members when 
<b>RasCustomScriptExecute</b> returns.


### -param pvReserved








#### - pRasCustomScriptExtensions [in]

Pointer to a 
<a href="https://msdn.microsoft.com/e143c1d7-1d4a-43e6-b099-3b65bb30dc06">RASCUSTOMSCRIPTEXTENSIONS</a> structure. This structure contains pointers to additional functions for the custom-scripting DLL.

<b>Windows 2000:  </b>This parameter is supported on Windows SP2 and later.


## -returns



If the function succeeds, the return value should be <b>ERROR_SUCCESS</b>.

If the function fails, the return value should be an appropriate error code from Winerror.h or Raserror.h.




## -remarks



When RAS calls 
<b>RasCustomScriptExecute</b>, the <i>pRasDialParams</i> parameter will point to the Unicode 
<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> structure. That is, the structure contains only Unicode strings.

In some cases, the <b>szUserName</b> of the 
<a href="https://msdn.microsoft.com/13d15c98-a41b-4bc8-8be6-c0b718b86fea">RASDIALPARAMS</a> structure will be an empty string. In these cases, the custom-scripting DLL should use the Unicode version of the 
<a href="_win32_getusername">GetUserName</a> function to obtain the name of the current user.




## -see-also




<a href="https://msdn.microsoft.com/c27b8b02-6018-4441-a355-1fb890b9001c">RAS Custom-Scripting</a>



<a href="https://msdn.microsoft.com/aba43ef9-7f62-48ab-a790-c8592a57f2c2">RasFreeBuffer</a>



<a href="https://msdn.microsoft.com/655f2dfa-a6cf-43db-8d2e-bf9a10163c75">RasGetBuffer</a>



<a href="https://msdn.microsoft.com/cc5523df-748d-4f96-8d54-bf0a2f9ecde4">RasReceiveBuffer</a>



<a href="https://msdn.microsoft.com/5dc8a034-f1cb-47c5-8d60-06f314a85f11">RasRetrieveBuffer</a>



<a href="https://msdn.microsoft.com/157a2bc7-351f-4170-b85b-ed789b4997ab">RasSendBuffer</a>
 

 

