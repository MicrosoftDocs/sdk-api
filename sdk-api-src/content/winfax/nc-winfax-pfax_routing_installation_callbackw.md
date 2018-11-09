---
UID: NC:winfax.PFAX_ROUTING_INSTALLATION_CALLBACKW
title: PFAX_ROUTING_INSTALLATION_CALLBACKW
author: windows-sdk-content
description: The FaxRoutingInstallationCallback function is a library-defined callback function that the FaxRegisterRoutingExtension function calls to install a fax routing extension DLL.
old-location: fax\_mfax_faxroutinginstallationcallback.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9aqz.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: FaxRoutingInstallationCallback, PFAX_ROUTING_INSTALLATION_CALLBACKW, PFAX_ROUTING_INSTALLATION_CALLBACKW callback, PFAX_ROUTING_INSTALLATION_CALLBACKW callback function [Fax Service], _mfax_faxroutinginstallationcallback, fax._mfax_faxroutinginstallationcallback, winfax/PFAX_ROUTING_INSTALLATION_CALLBACKW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winfax.h
api_name:
 - PFAX_ROUTING_INSTALLATION_CALLBACKW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFAX_ROUTING_INSTALLATION_CALLBACKW callback function


## -description


The <i>FaxRoutingInstallationCallback</i> function is a library-defined callback function that the <a href="https://msdn.microsoft.com/27158cf3-9616-499e-8cd9-4eee60bf1f44">FaxRegisterRoutingExtension</a> function calls to install a fax routing extension DLL. <b>FaxRegisterRoutingExtension</b> calls the <i>FaxRoutingInstallationCallback</i> function multiple times, once for each fax routing method the fax routing extension exports.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function.


### -param Context [in]

Type: <b>LPVOID</b>

Pointer to a variable that contains application-specific context information or an application-defined value. The <a href="https://msdn.microsoft.com/27158cf3-9616-499e-8cd9-4eee60bf1f44">FaxRegisterRoutingExtension</a> function passes this data to the <i>FaxRoutingInstallationCallback</i> function.


### -param MethodName [out]

Type: <b>LPWSTR</b>

Pointer to a variable to receive a null-terminated Unicode character string that specifies the internal name of the fax routing method. The string must not exceed 100 characters. For information about fax routing methods, see <a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">About the Fax Routing Extension API</a>.


### -param FriendlyName [out]

Type: <b>LPWSTR</b>

Pointer to a variable to receive a null-terminated Unicode character string that specifies the user-friendly name to display for the fax routing method. The string must not exceed 100 characters.


### -param FunctionName [out]

Type: <b>LPWSTR</b>

Pointer to a variable to receive a null-terminated Unicode character string. The string contains the name of the exported function that executes the specified fax routing procedure. The string must not exceed 100 characters.


### -param Guid [out]

Type: <b>LPWSTR</b>

Pointer to a variable to receive a null-terminated Unicode character string. The string specifies the GUID that uniquely identifies the fax routing method of interest.


## -returns



Type: <b>BOOL</b>

The <i>FaxRoutingInstallationCallback</i> function returns a value of nonzero to indicate that the <a href="https://msdn.microsoft.com/27158cf3-9616-499e-8cd9-4eee60bf1f44">FaxRegisterRoutingExtension</a> function should register the fax routing method for the fax routing extension, using the data pointed to by the parameters.

The function returns a value of zero to indicate that there are no more fax routing methods to register, and calls to <i>FaxRoutingInstallationCallback</i> should be terminated.




## -remarks



The <b>PFAX_ROUTING_INSTALLATION_CALLBACKW</b> data type is a pointer to a <i>FaxRoutingInstallationCallback</i> function.

A fax client application specifies the <i>FaxRoutingInstallationCallback</i> function by passing its address when it calls the <a href="https://msdn.microsoft.com/27158cf3-9616-499e-8cd9-4eee60bf1f44">FaxRegisterRoutingExtension</a> function. For more information, see <a href="https://msdn.microsoft.com/797a4d48-7676-4b0d-93bf-ebe3043da4a0">Registration of a Fax Routing Extension</a>.

For information about fax routing extensions, see <a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">About the Fax Routing Extension API</a>.




## -see-also




<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/27158cf3-9616-499e-8cd9-4eee60bf1f44">FaxRegisterRoutingExtension</a>
 

 

