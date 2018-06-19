---
UID: NF:msclus.ISClusPropertyValue.get_Length
title: ISClusPropertyValue::get_Length
author: windows-sdk-content
description: Size of a property value.
old-location: mscs\cluspropertyvalue_length.htm
old-project: MsCS
ms.assetid: c9c2e4b8-71db-4d28-80ac-f774af573871
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusPropertyValue object [Failover Cluster],Length property, ClusPropertyValue.Length, ISClusPropertyValue.get_Length, ISClusPropertyValue::get_Length, Length property [Failover Cluster], Length property [Failover Cluster],ClusPropertyValue object, _wolf_cluspropertyvalue.length, get_Length, mscs.cluspropertyvalue_length
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
 - ClusPropertyValue.Length
 - ISClusPropertyValue.get_Length
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusPropertyValue::get_Length


## -description


<p class="CCE_Message">[The <b>Length</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns the byte 
    size of a <a href="/windows/desktop/dns/p-gly">property value</a>.

This property is read-only.


## -parameters


## -remarks



The <b>Length</b> property corresponds to the 
    <b>cbLength</b> member of a 
    <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/6a8ffae6-c4f3-42fb-9703-eeb695902877">ClusPropertyValue</a>
 

 

