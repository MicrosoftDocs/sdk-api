---
UID: NE:comsvcs.tagCSC_SxsConfig
title: tagCSC_SxsConfig
author: windows-sdk-content
description: Indicates how side-by-side assemblies are configured for CServiceConfig.
old-location: cos\csc_sxsconfig.htm
tech.root: cossdk
ms.assetid: 8c114e9e-b201-4317-8a45-d5b0964c6ff8
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CSC_InheritSxs, CSC_NewSxs, CSC_NoSxs, CSC_SxsConfig, CSC_SxsConfig enumeration [COM+], _cos_CSC_SxsConfig, comsvcs/CSC_InheritSxs, comsvcs/CSC_NewSxs, comsvcs/CSC_NoSxs, comsvcs/CSC_SxsConfig, cos.csc_sxsconfig, tagCSC_SxsConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CSC_SxsConfig
product: Windows
targetos: Windows
req.typenames: CSC_SxsConfig
req.redist: 
---

# tagCSC_SxsConfig enumeration


## -description


Indicates how side-by-side assemblies are configured for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>.


## -enum-fields




### -field CSC_NoSxs

Side-by-side assemblies are not used within the enclosed context. This is the default setting for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Ignore.


### -field CSC_InheritSxs

The current side-by-side assembly of the enclosed context is used. This is the default setting for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Inherit.


### -field CSC_NewSxs

A new side-by-side assembly is created for the enclosed context.


## -remarks



This enumeration is used to configure side-by-side assemblies through <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> for either the work submitted through the activity created by <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or the work that is enclosed between calls to <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> and <a href="https://msdn.microsoft.com/b67b3cf6-4462-4578-b61b-c5c61d809822">CoLeaveServiceDomain</a>.




## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/24d4a22b-0a01-4bf2-9cc6-4a1b31897d05">IServiceSxSConfig::SxSConfig</a>



<a href="https://msdn.microsoft.com/2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0">Isolated Applications and Side-by-side Assemblies</a>
 

 

