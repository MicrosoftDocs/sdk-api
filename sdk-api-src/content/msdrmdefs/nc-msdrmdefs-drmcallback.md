---
UID: NC:msdrmdefs.DRMCALLBACK
title: DRMCALLBACK
author: windows-sdk-content
description: Some of the functions included in the AD RMS SDK provide status information and licenses to your application by using a callback function that you must implement. The callback syntax is shown below.
old-location: rm\callback_prototype.htm
tech.root: AdRms_Sdk
ms.assetid: 41c200df-afbc-43a5-8046-d131fec3261a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DRM callback, DRMCallback, DRMCallback callback function [Active Directory Rights Management Services SDK 1.0], msdrmdefs/DRMCallback, rm.callback_prototype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: msdrmdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - Msdrmdefs.h
api_name:
 - DRMCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMCALLBACK callback function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

Some of the functions included in the AD RMS SDK provide status information and licenses to your application by using a callback function that you must implement. The callback syntax is shown below.


## -parameters




### -param Arg1


### -param Arg2


### -param *








#### - hr

The status of the current action.


#### - msg

Specifies the action being performed. This can be one of the <a href="https://msdn.microsoft.com/9420c415-09ef-43a0-b458-bfaae9857314">DRM_STATUS_MSG</a> enumeration values.


#### - pvContext

An application-defined value, such as a pointer to a callback function or a pointer to an event handle.


#### - pvParam

This parameter depends on the action being processed. For more information, see the specific message value in the <a href="https://msdn.microsoft.com/9420c415-09ef-43a0-b458-bfaae9857314">DRM_STATUS_MSG</a> enumeration.


## -returns



 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The following asynchronous AD RMS functions use a callback function:

<ul>
<li>
<a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3ed180d1-27c9-4f39-b353-1d417636ca62">DRMGetSignedIssuanceLicense</a>
</li>
<li>
<a href="https://msdn.microsoft.com/42c58096-429c-4278-b9ab-8c5a91361af8">DRMAcquireAdvisories</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d3f4ac2c-95d9-4273-a679-81670dd62d28">DRMActivate</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/7d880b74-1934-4282-a7ca-1dac3602d6b4">Creating a Callback Function</a>



<a href="https://msdn.microsoft.com/14688148-25fa-4f11-9a0f-9b284a307175">End-User License Callback Example</a>



<a href="https://msdn.microsoft.com/c46695fd-5e9f-4d0b-94fe-a5f961ab7e76">Issuance License Callback Example</a>
 

 

