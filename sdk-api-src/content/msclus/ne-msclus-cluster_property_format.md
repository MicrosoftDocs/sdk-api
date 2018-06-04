---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# CLUSTER_PROPERTY_FORMAT enumeration


## -description


Specifies the data type of a property value in a 
    <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a>.


## -enum-fields




### -field CLUSPROP_FORMAT_UNKNOWN

Data is in an unknown format.


### -field CLUSPROP_FORMAT_BINARY

Data is a binary value.


### -field CLUSPROP_FORMAT_DWORD

Data is a <b>DWORD</b> value.


### -field CLUSPROP_FORMAT_SZ

Data is a null-terminated Unicode string.


### -field CLUSPROP_FORMAT_EXPAND_SZ

Data is a null-terminated Unicode string with unexpanded references to environment variables.


### -field CLUSPROP_FORMAT_MULTI_SZ

Data is an array of null-terminated Unicode strings.


### -field CLUSPROP_FORMAT_ULARGE_INTEGER

Data is an <b>ULARGE_INTEGER</b>.


### -field CLUSPROP_FORMAT_LONG

Data is an signed <b>LONG</b> value.


### -field CLUSPROP_FORMAT_EXPANDED_SZ

Data is a null-terminated Unicode string with expanded references to environment variables.


### -field CLUSPROP_FORMAT_SECURITY_DESCRIPTOR

Data is a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> in 
          <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative</a> 
          format. For more information about self-relative security descriptors, see 
          <a href="https://msdn.microsoft.com/dab2844b-7df9-446c-aacf-380a0a805cbc">Absolute and Self-Relative Security Descriptors</a>.


### -field CLUSPROP_FORMAT_LARGE_INTEGER

Data is a signed <b>LARGE_INTEGER</b>.


### -field CLUSPROP_FORMAT_WORD

Data is a <b>WORD</b> value.


### -field CLUSPROP_FORMAT_FILETIME

Data is a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>.


### -field CLUSPROP_FORMAT_VALUE_LIST


### -field CLUSPROP_FORMAT_PROPERTY_LIST


### -field CLUSPROP_FORMAT_USER

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/259aba6f-b1a6-422d-859b-8e6c95895ab5">Format Property of the ClusProperty Object</a>



<a href="https://msdn.microsoft.com/a53a969b-9269-43c7-81a0-178e61a23058">Format Property of the ClusPropertyValue Object</a>
 

 

