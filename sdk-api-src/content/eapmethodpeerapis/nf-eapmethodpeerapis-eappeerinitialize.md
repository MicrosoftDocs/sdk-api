---
UID: NF:eapmethodpeerapis.EapPeerInitialize
title: EapPeerInitialize function
author: windows-sdk-content
description: Initializes an EAP peer method for EAPHost.
old-location: eaphost\eappeerinitialize.htm
tech.root: EAPHost
ms.assetid: 7c040f9c-1a70-4882-bea1-7e641f5b1d3f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EapPeerInitialize, EapPeerInitialize function [EAPHost], eaphost.eappeerinitialize, eapmethodpeerapis/EapPeerInitialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: eapmethodpeerapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - eapmethodpeerapis.h
api_name:
 - EapPeerInitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapPeerInitialize function


## -description


Initializes an EAP peer  method for EAPHost.


## -parameters




### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



 An EAP method is a DLL that implements and exports the EAP Peer Method APIs. Example methods include MS-PEAPv0 and later, MS-EAP-TLS, and MS-CHAPv2. You can also create and implement custom EAP methods, as well.

The EAP method libraries together with EAPHOST.dll make up the "EAPHost". The host DLL manages the libraries and allows supplicants (EAP clients) to authenticate against them.

Each API is handled as a function pointer by EAPHost, who calls them if they conform to the specific signatures and calling conventions specified in this documentation. These function pointers are obtained when EAPHost calls <a href="https://msdn.microsoft.com/99b7e136-b502-435b-9c62-a0e106ec8ec5">EapPeerGetInfo</a>.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/fdfa595d-acf7-4489-88a8-113093567fe5">EAPHost Peer Method Run-Time Functions</a>
 

 

