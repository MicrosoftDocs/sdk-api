---
UID: NF:msclus.ISClusProperty.get_Format
title: ISClusProperty::get_Format
author: windows-sdk-content
description: The format (data type) of a cluster object property.
old-location: mscs\clusproperty_format.htm
old-project: MsCS
ms.assetid: 259aba6f-b1a6-422d-859b-8e6c95895ab5
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: CLUSPROP_FORMAT_BINARY, CLUSPROP_FORMAT_DWORD, CLUSPROP_FORMAT_EXPANDED_SZ, CLUSPROP_FORMAT_EXPAND_SZ, CLUSPROP_FORMAT_FILETIME, CLUSPROP_FORMAT_LARGE_INTEGER, CLUSPROP_FORMAT_LONG, CLUSPROP_FORMAT_MULTI_SZ, CLUSPROP_FORMAT_SECURITY_DESCRIPTOR, CLUSPROP_FORMAT_SZ, CLUSPROP_FORMAT_ULARGE_INTEGER, CLUSPROP_FORMAT_UNKNOWN, CLUSPROP_FORMAT_USER, CLUSPROP_FORMAT_WORD, ClusProperty object [Failover Cluster],Format property, ClusProperty.Format, Format property [Failover Cluster], Format property [Failover Cluster],ClusProperty object, ISClusProperty.get_Format, ISClusProperty::get_Format, _wolf_clusproperty.format, get_Format, mscs.clusproperty_format
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusProperty.Format
 - ISClusProperty.get_Format
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperty::get_Format


## -description


<p class="CCE_Message">[The <b>Format</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Returns or sets 
    the format (data type) of a 
    <a href="https://msdn.microsoft.com/ba11ba7a-10f7-4f2c-99cd-d274912ad454">cluster object property</a>.

This property is read-only.


## -parameters


## -remarks



The <b>Format</b> property corresponds to the 
    <b>wFormat</b> member of a 
    <a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a> union.

For information on making constants defined by the Cluster Automation Server type library (MsClus.tlb) 
    available to scripts, see 
    <a href="https://msdn.microsoft.com/2ca508c9-c34a-4af5-a6c0-3d710171f3df">Creating a Cluster Automation Server Script</a>.




## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a>



<a href="https://msdn.microsoft.com/4cae1bb4-2ca4-4957-b174-1dc07676ce3a">ClusProperty.Type</a>
 

 

