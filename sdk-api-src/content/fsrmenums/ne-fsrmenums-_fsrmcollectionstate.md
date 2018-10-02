---
UID: NE:fsrmenums._FsrmCollectionState
title: "_FsrmCollectionState"
author: windows-sdk-content
description: Defines the possible states of a collection object.
old-location: fsrm\fsrmcollectionstate.htm
tech.root: Fsrm
ms.assetid: 94d7cf83-7fa4-4fec-956d-f5b2e2c0bf68
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FsrmCollectionState, FsrmCollectionState enumeration [File Server Resource Manager], FsrmCollectionState_Cancelled, FsrmCollectionState_Committing, FsrmCollectionState_Complete, FsrmCollectionState_Fetching, _FsrmCollectionState, fs.fsrmcollectionstate, fsrm.fsrmcollectionstate, fsrmenums/FsrmCollectionState, fsrmenums/FsrmCollectionState_Cancelled, fsrmenums/FsrmCollectionState_Committing, fsrmenums/FsrmCollectionState_Complete, fsrmenums/FsrmCollectionState_Fetching
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmCollectionState
product: Windows
targetos: Windows
req.typenames: FsrmCollectionState
req.redist: 
---

# _FsrmCollectionState enumeration


## -description


Defines the possible states of a collection object.


## -enum-fields




### -field FsrmCollectionState_Fetching

The collection object is fetching data.


### -field FsrmCollectionState_Committing

The collection object is committing its data.


### -field FsrmCollectionState_Complete

The collection object is complete (has stopped fetching or committing data).


### -field FsrmCollectionState_Cancelled

The collection operation (fetching or committing) was canceled.


## -see-also




<a href="https://msdn.microsoft.com/c12c55c1-baff-4810-ad2a-453abb6af5b5">IFsrmCollection::State</a>
 

 

