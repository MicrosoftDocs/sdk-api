---
UID: NF:winfax.FaxRegisterServiceProviderW
title: FaxRegisterServiceProviderW function
author: windows-sdk-content
description: The FaxRegisterServiceProvider function registers a fax service provider DLL with the fax service. The function configures the fax service registry to query and use the new fax service provider DLL when the fax service restarts.
old-location: fax\_mfax_faxregisterserviceprovider.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_94xe.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FaxRegisterServiceProvider, FaxRegisterServiceProvider function [Fax Service], FaxRegisterServiceProviderW, _mfax_faxregisterserviceprovider, fax._mfax_faxregisterserviceprovider, winfax/FaxRegisterServiceProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winfax.h
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
tech.root: 
req.typenames: EVT_VARIANT, *PEVT_VARIANT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - WinFax.lib
 - WinFax.dll
api_name:
 - FaxRegisterServiceProvider
product: Windows
targetos: Windows
req.lib: WinFax.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FaxRegisterServiceProviderW function


## -description


The <b>FaxRegisterServiceProvider</b> function registers a fax service provider DLL with the fax service. The function configures the fax service registry to query and use the new fax service provider DLL when the fax service restarts.


## -parameters




### -param DeviceProvider [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the internal name of the fax service provider DLL to register. This should be a unique string, such as a GUID.


### -param FriendlyName [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string to associate with the fax service provider DLL. This is the fax service provider's user-friendly name, suitable for display.


### -param ImageName [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the full path and file name for the fax service provider DLL. The path can include valid environment variables, for example, %SYSTEMDRIVE% and %SYSTEMROOT%.


### -param TspName [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the name of the telephony service provider associated with the devices for the fax service provider. For a virtual fax device, use an empty string.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter to the <a href="https://msdn.microsoft.com/1128f91b-2ebf-4c51-acd7-7c724560b870">FaxRegisterServiceProvider</a> function is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Because the <b>FaxRegisterServiceProvider</b> function modifies the registry, the user, generally a system administrator, must have write access to the <b>HKEY_LOCAL_MACHINE</b> registry key.

All parameters to the <b>FaxRegisterServiceProvider</b> function are required.

Local installation of a fax service provider is recommended. The local installation routine for a fax service provider DLL can call <b>FaxRegisterServiceProvider</b> instead of directly accessing the registry. For more information about the steps required to register locally with the fax service, see <a href="https://msdn.microsoft.com/13bfb897-11f5-4fce-ac6e-8fbec7413e13">Registration of a Fax Service Provider</a>.




## -see-also




<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>
 

 

