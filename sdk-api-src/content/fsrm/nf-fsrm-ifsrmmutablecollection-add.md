---
UID: NF:fsrm.IFsrmMutableCollection.Add
title: IFsrmMutableCollection::Add
author: windows-driver-content
description: Adds an object to the collection.
old-location: fsrm\ifsrmmutablecollection_add.htm
old-project: Fsrm
ms.assetid: 916f01de-c87c-450c-859a-c349a165f91d
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: Add, Add method [File Server Resource Manager], Add method [File Server Resource Manager],IFsrmMutableCollection interface, IFsrmMutableCollection interface [File Server Resource Manager],Add method, IFsrmMutableCollection.Add, IFsrmMutableCollection::Add, fs.ifsrmmutablecollection_add, fsrm.ifsrmmutablecollection_add, fsrm/IFsrmMutableCollection::Add
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
req.typenames: FILTERED_DATA_SOURCES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmMutableCollection.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmMutableCollection::Add


## -description


Adds an object to the collection.


## -parameters




### -param item [in]

A <b>VARIANT</b> that contains the <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface of the object to add to the collection. Set the variant type to <b>VT_DISPATCH</b> and the <b>pdispVal</b> member to the <b>IDispatch</b> interface of the object.


## -returns



The method returns the following return values.




## -remarks



All items in the collection must be of the same type.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/c76c0cc5-1109-46ec-be4d-c6c5f14a6df7">Using Templates to Define File Screens</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e41f01ef-5dd2-4066-82cd-45b57578c9bb">IFsrmMutableCollection</a>
 

 

