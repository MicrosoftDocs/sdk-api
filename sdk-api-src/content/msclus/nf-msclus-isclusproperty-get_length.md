---
UID: NF:msclus.ISClusProperty.get_Length
title: ISClusProperty::get_Length
author: windows-sdk-content
description: Size of a cluster object property.
old-location: mscs\clusproperty_length.htm
old-project: mscs
ms.assetid: 9e2d1aec-8644-43e9-a079-82cf96e43e4e
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusProperty object [Failover Cluster],Length property, ClusProperty.Length, ISClusProperty.get_Length, ISClusProperty::get_Length, Length property [Failover Cluster], Length property [Failover Cluster],ClusProperty object, _wolf_clusproperty.length, get_Length, mscs.clusproperty_length
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
 - ClusProperty.Length
 - ISClusProperty.get_Length
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperty::get_Length


## -description


<p class="CCE_Message">[The <b>Length</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Returns the byte 
    size of a 
    <a href="https://msdn.microsoft.com/ba11ba7a-10f7-4f2c-99cd-d274912ad454">cluster object property</a>.

This property is read-only.


## -parameters


## -remarks



The <b>Length</b> property corresponds to the 
    <b>cbLength</b> member of a 
    <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a>
 

 

