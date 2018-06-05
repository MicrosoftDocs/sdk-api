---
UID: NS:clusapi._CLUS_CSV_VOLUME_NAME
title: "_CLUS_CSV_VOLUME_NAME"
author: windows-sdk-content
description: Represents the name of a cluster shared volume (CSV).
old-location: mscs\clus_csv_volume_name.htm
old-project: MsCS
ms.assetid: 18E17AA6-1244-41EA-918E-7BDBB90A0D70
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PCLUS_CSV_VOLUME_NAME, CLUS_CSV_VOLUME_NAME, CLUS_CSV_VOLUME_NAME structure [Failover Cluster], PCLUS_CSV_VOLUME_NAME, PCLUS_CSV_VOLUME_NAME structure pointer [Failover Cluster], _CLUS_CSV_VOLUME_NAME, clusapi/CLUS_CSV_VOLUME_NAME, clusapi/PCLUS_CSV_VOLUME_NAME, mscs.clus_csv_volume_name"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
req.typenames: CLUS_CSV_VOLUME_NAME, *PCLUS_CSV_VOLUME_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ClusAPI.h
api_name:
-	CLUS_CSV_VOLUME_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CLUS_CSV_VOLUME_NAME structure


## -description


Represents the name of a cluster shared volume (CSV).


## -struct-fields




### -field VolumeOffset

The physical offset, in bytes, of the data on the CSV.


### -field szVolumeName

A Unicode string that contains the volume name of the CSV. The string has a terminating null character.  The name provided can be either the cluster-assigned friendly name or the volume <b>GUID</b> path of the form "\\?\Volume{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}\".


### -field szRootPath

The root path of the CSV.


## -see-also




<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

