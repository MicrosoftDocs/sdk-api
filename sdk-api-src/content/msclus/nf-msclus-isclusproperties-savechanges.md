---
UID: NF:msclus.ISClusProperties.SaveChanges
title: ISClusProperties::SaveChanges
author: windows-sdk-content
description: Updates the cluster database with the property data currently stored in the ClusProperties collection.
old-location: mscs\clusproperties_savechanges.htm
old-project: mscs
ms.assetid: 2792025f-c434-47e0-a5e8-06a992e3a8d2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusProperties collection [Failover Cluster],SaveChanges method, ClusProperties.SaveChanges, ISClusProperties.SaveChanges, ISClusProperties::SaveChanges, SaveChanges, SaveChanges method [Failover Cluster], SaveChanges method [Failover Cluster],ClusProperties collection, _wolf_clusproperties.savechanges, mscs.clusproperties_savechanges
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.redist: 
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
 - ClusProperties.SaveChanges
 - ISClusProperties.SaveChanges
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperties::SaveChanges


## -description


<p class="CCE_Message">[The <b>SaveChanges</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Updates 
    the <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> with the property data currently 
    stored in the <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> 
    collection.


## -parameters




### -param pvarStatusCode






## -returns



This method does not return a value.




## -remarks



A <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection contains a 
    local copy of property data. Changes to the data do not take effect in the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a> until 
    <b>ClusProperties.SaveChanges</b> is called.

If the properties are successfully saved, 
    <b>ClusProperties.SaveChanges</b> calls the 
    <a href="https://msdn.microsoft.com/900c9401-e8f4-423a-80df-598f5edb2935">ClusProperties.Refresh</a> method.

The <b>ClusProperties.SaveChanges</b> method 
    will fail if the properties in the collection are read-only.




## -see-also




<a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a>
 

 

