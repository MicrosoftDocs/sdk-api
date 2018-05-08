---
UID: NC:ntsecpkg.SpValidateTargetInfoFn
title: SpValidateTargetInfoFn
author: windows-driver-content
description: Validates that the specified SECPKG_TARGETINFO structure represents a valid target.
old-location: security\spvalidatetargetinfofn.htm
old-project: SecAuthN
ms.assetid: 01d1b74a-14d9-40cd-bcca-a031f5fc9cbb
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: SpValidateTargetInfoFn, SpValidateTargetInfoFn function [Security], ntsecpkg/SpValidateTargetInfoFn, security.spvalidatetargetinfofn
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	SpValidateTargetInfoFn
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SpValidateTargetInfoFn callback function


## -description


Validates that the specified <a href="https://msdn.microsoft.com/c8d4ac70-743b-42b1-940c-d3d37a6174bc">SECPKG_TARGETINFO</a> structure represents a valid target.


## -parameters




### -param ClientRequest [in, optional]

A pointer to an opaque 
<a href="https://msdn.microsoft.com/384dd6e0-726f-4100-a036-1cca6a332a64">LSA_CLIENT_REQUEST</a> data structure that contains information about the LSA client's authentication request. A custom authentication package should pass in the value received during the client's call to the function, such as 
<a href="https://msdn.microsoft.com/be0f9886-c0f6-4361-96c7-d16da8713fc7">LsaApCallPackage</a> or 
<a href="https://msdn.microsoft.com/4c8def77-d536-486e-a830-9df3848fbccb">LsaApLogonUser</a>, that returns the output parameter.


### -param ProtocolSubmitBuffer [in]

A pointer to the input buffer sent by the client.


### -param ClientBufferBase [in]

The base address of the input buffer, in the client's address space.


### -param SubmitBufferLength [in]

The size, in bytes, of the <i>ProtocolSubmitBuffer</i> buffer.


### -param TargetInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/c8d4ac70-743b-42b1-940c-d3d37a6174bc">SECPKG_TARGETINFO</a> structure that specifies the target to validate.


## -returns




						If the function succeeds and the specified target is a valid target, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



SSP/APs must implement the <b>SpValidateTargetInfo</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpValidateTargetInfo</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>
 

 

