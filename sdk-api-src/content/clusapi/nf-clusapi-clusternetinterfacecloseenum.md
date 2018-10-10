---
UID: NF:clusapi.ClusterNetInterfaceCloseEnum
title: ClusterNetInterfaceCloseEnum function
author: windows-sdk-content
description: Closes a network interface enumeration handle.
old-location: mscs\clusternetinterfacecloseenum.htm
tech.root: MsCS
ms.assetid: da7819b5-0f18-44e3-83e7-f6d5ccbc0de6
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ClusterNetInterfaceCloseEnum, ClusterNetInterfaceCloseEnum function [Failover Cluster], clusapi/ClusterNetInterfaceCloseEnum, mscs.clusternetinterfacecloseenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterNetInterfaceCloseEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterNetInterfaceCloseEnum function


## -description


Closes a  network interface enumeration handle.


## -parameters




### -param hNetInterfaceEnum [in]

Handle to the node enumerator to close. This is a handle originally returned by the  <a href="https://msdn.microsoft.com/fd300162-2472-4bd2-91d6-357397c4134c">ClusterNetInterfaceOpenEnum</a> function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.
     If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.



