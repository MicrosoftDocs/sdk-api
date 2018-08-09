---
UID: NF:msclus.ISClusResTypes.CreateItem
title: ISClusResTypes::CreateItem
author: windows-sdk-content
description: Creates a new resource type in the cluster and adds it to a ClusResTypes collection.
old-location: mscs\clusrestypes_createitem.htm
old-project: mscs
ms.assetid: f7fc79b1-1803-4060-bf1f-39a253bccab6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResTypes collection [Failover Cluster],CreateItem method, ClusResTypes.CreateItem, CreateItem, CreateItem method [Failover Cluster], CreateItem method [Failover Cluster],ClusResTypes collection, ISClusResTypes.CreateItem, ISClusResTypes::CreateItem, _wolf_clusrestypes.createitem, mscs.clusrestypes_createitem
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
 - ClusResTypes.CreateItem
 - ISClusResTypes.CreateItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResTypes::CreateItem


## -description


<p class="CCE_Message">[The <b>CreateItem</b> method 
    is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable 
    in subsequent versions.]

Creates a new 
    <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> in the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and adds it to a 
    <a href="https://msdn.microsoft.com/614d3ed6-255f-46ed-9354-7a73a21cac87">ClusResTypes</a> collection.


## -parameters




### -param bstrResourceTypeName




### -param bstrDisplayName




### -param bstrResourceTypeDll




### -param dwLooksAlivePollInterval




### -param dwIsAlivePollInterval




### -param ppResourceType






#### - strResTypeName

String containing the name of the new resource type.


#### - strDisplayName

String containing the display name of the new resource type.


#### - strResTypeDll

String containing the file name of the library containing the new resource type.


#### - lLooksAlivePollInterval

Length of time in milliseconds that should occur between calls to the new resource type's 
      <a href="https://msdn.microsoft.com/cfc57325-847d-4f59-bee8-6a02b0a2ef32">LooksAlive</a> entry point function.


#### - lIsAlivePollInterval

Length of time in milliseconds that should occur between calls to the new resource type's 
      <a href="https://msdn.microsoft.com/ff7661af-0a24-4a2e-bb31-c967845a4ff4">IsAlive</a> entry point function.


## -returns



A <a href="https://msdn.microsoft.com/e4ad6364-f318-47f9-a276-d99c91ffbbb5">ClusResType</a> object that receives the newly 
      added resource type.




## -remarks



The new resource type must be supported by a 
    <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a>. For more information, see 
    <a href="https://msdn.microsoft.com/de3569ef-ee74-457e-b672-00e22ee8154c">Creating a Custom Resource Type</a>.




## -see-also




<a href="https://msdn.microsoft.com/e4ad6364-f318-47f9-a276-d99c91ffbbb5">ClusResType</a>



<a href="https://msdn.microsoft.com/614d3ed6-255f-46ed-9354-7a73a21cac87">ClusResTypes</a>



<a href="https://msdn.microsoft.com/ff7661af-0a24-4a2e-bb31-c967845a4ff4">IsAlive</a>



<a href="https://msdn.microsoft.com/cfc57325-847d-4f59-bee8-6a02b0a2ef32">LooksAlive</a>
 

 

