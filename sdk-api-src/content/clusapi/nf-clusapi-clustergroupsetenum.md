---
UID: NF:clusapi.ClusterGroupSetEnum
title: ClusterGroupSetEnum function
author: windows-sdk-content
description: Returns the next enumerable object.
old-location: mscs\clustergroupcollectionenum.htm
tech.root: MsCS
ms.assetid: 926f67bd-2933-4b95-8320-166fe5299d7a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ClusterGroupCollectionEnum, ClusterGroupCollectionEnum function [Failover Cluster], ClusterGroupSetEnum, clusapi/ClusterGroupCollectionEnum, mscs.clustergroupcollectionenum
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
 - ClusterGroupCollectionEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ClusterGroupSetEnum
: 
---

# ClusterGroupSetEnum function


## -description


Returns the next enumerable object.


## -parameters




### -param hGroupSetEnum [in]

A handle to an open cluster node enumeration
    returned by <a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a>



### -param dwIndex [in]

The index to enumerate, zero for the first call to this function and then
    incremented for subsequent calls.


### -param lpszName [out]

Points to a buffer that receives the name of the object,
    including the terminating null character.


### -param lpcchName [in, out]

Points to a variable that specifies the size, in characters,
    of the buffer pointed to by the <i>lpszName</i> parameter. This size
    should include the terminating null character. When the function
    returns, the variable contains the
    number of characters stored in the buffer, not including the terminating null character.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.



