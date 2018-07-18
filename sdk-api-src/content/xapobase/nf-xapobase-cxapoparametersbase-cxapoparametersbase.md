---
UID: NF:xapobase.CXAPOParametersBase.CXAPOParametersBase
title: CXAPOParametersBase::CXAPOParametersBase
author: windows-sdk-content
description: Creates an instance of the CXAPOParametersBase class.
old-location: xaudio2\cxapoparametersbase_cxapoparametersbase.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase.CXAPOParametersBase(BYTE,UINT32,BOOL)
ms.author: windowssdkdev
ms.date: 04/23/2018
ms.keywords: CXAPOParametersBase, CXAPOParametersBase interface [XAudio2 Audio Mixing APIs],CXAPOParametersBase method, CXAPOParametersBase method [XAudio2 Audio Mixing APIs], CXAPOParametersBase method [XAudio2 Audio Mixing APIs],CXAPOParametersBase interface, CXAPOParametersBase.CXAPOParametersBase, CXAPOParametersBase::CXAPOParametersBase, xapobase/CXAPOParametersBase::CXAPOParametersBase, xaudio2.cxapoparametersbase_cxapoparametersbase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xapobase.h
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
tech.root: 
req.typenames: XAPO_REGISTRATION_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPOBase.lib
 - XAPOBase.dll
api_name:
 - CXAPOParametersBase.CXAPOParametersBase
product: Windows
targetos: Windows
req.lib: XAPOBase.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# CXAPOParametersBase::CXAPOParametersBase


## -description


Creates an instance of the <a href="https://msdn.microsoft.com/70F46E4E-E4FC-434F-AB35-B32C1365BB6D">CXAPOParametersBase</a> class.


## -parameters




### -param pRegistrationProperties




### -param pParameterBlocks

Type: <b>BYTE*</b>

Pointer to three contiguous process parameter blocks used for synchronization.


### -param uParameterBlockByteSize

Type: <b>UINT32</b>

Size of a parameter block in <i>pParameterBlocks</i>.


### -param fProducer

Type: <b>BOOL</b>

If TRUE, indicates <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">IXAPO::Process</a> produces data to be returned by <a href="https://msdn.microsoft.com/FBF27BCD-6B20-4D8A-BD9D-8E0889889F8B">IXAPOParameters::GetParameters</a> and disallows calls to <a href="https://msdn.microsoft.com/1E6FD9FB-9E99-422E-B2E1-3679FC3EEF32">IXAPOParameters::SetParameters</a>.


#### - pRegProperties

Type: <b>const XAPO_REGISTRATION_PROPERTIES*</b>

A pointer to an <a href="https://msdn.microsoft.com/2824919b-a4ec-4fee-93d2-6157340f2d43">XAPO_REGISTRATION_PROPERTIES</a> structure that contains the registration properties for the XAPO. 


## -returns



This method does not return a value.




## -remarks



All process parameter blocks in <i>pParameterBlocks</i> must be initialized to the same default value before there is a call to the <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">IXAPO::Process</a>, <a href="https://msdn.microsoft.com/FBF27BCD-6B20-4D8A-BD9D-8E0889889F8B">IXAPOParameters::GetParameters</a>, and <a href="https://msdn.microsoft.com/1E6FD9FB-9E99-422E-B2E1-3679FC3EEF32">IXAPOParameters::SetParameters</a> methods. Usually this initialization should be handled in <a href="https://msdn.microsoft.com/4C975ED7-5656-4C48-A402-99011B7D37AF">IXAPO::Initialize</a> or in <a href="https://msdn.microsoft.com/2143A204-342F-4A78-A6D7-D319360A3948">IXAPO::LockForProcess</a>.



The object created by this <a href="https://msdn.microsoft.com/70F46E4E-E4FC-434F-AB35-B32C1365BB6D">CXAPOParametersBase</a> will have a reference count of 1.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/70F46E4E-E4FC-434F-AB35-B32C1365BB6D">CXAPOParametersBase</a>
 

 

