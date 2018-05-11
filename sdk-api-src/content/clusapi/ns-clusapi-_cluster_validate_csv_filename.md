---
UID: NS:clusapi._CLUSTER_VALIDATE_CSV_FILENAME
title: "_CLUSTER_VALIDATE_CSV_FILENAME"
author: windows-driver-content
description: Represents a cluster shared volume (CSV) during a validation operation.
old-location: mscs\cluster_validate_csv_filename.htm
old-project: MsCS
ms.assetid: E2FA02BE-45FC-4D0F-A6F3-870D20D1BCA5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PCLUSTER_VALIDATE_CSV_FILENAME, CLUSTER_VALIDATE_CSV_FILENAME, CLUSTER_VALIDATE_CSV_FILENAME structure [Failover Cluster], PCLUSTER_VALIDATE_CSV_FILENAME, PCLUSTER_VALIDATE_CSV_FILENAME structure pointer [Failover Cluster], _CLUSTER_VALIDATE_CSV_FILENAME, clusapi/CLUSTER_VALIDATE_CSV_FILENAME, clusapi/PCLUSTER_VALIDATE_CSV_FILENAME, mscs.cluster_validate_csv_filename"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CLUSTER_VALIDATE_CSV_FILENAME, *PCLUSTER_VALIDATE_CSV_FILENAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ClusApi.h
api_name:
-	CLUSTER_VALIDATE_CSV_FILENAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CLUSTER_VALIDATE_CSV_FILENAME structure


## -description


Represents a cluster shared volume (CSV) during a validation operation.


## -struct-fields




### -field szFileName

A  Unicode string that contains the volume name of the CSV. The string ends with a terminating null character.  The name provided can be either the cluster-assigned friendly name or the volume <b>GUID</b> path of the form "\\?\Volume{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}\".


## -see-also




<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 

