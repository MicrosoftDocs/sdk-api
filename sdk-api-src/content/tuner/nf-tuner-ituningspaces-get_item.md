---
UID: NF:tuner.ITuningSpaces.get_Item
title: ITuningSpaces::get_Item (tuner.h)
author: windows-sdk-content
description: The get_Item method returns the specified item in the collection.
old-location: mstv\ituningspaces_get_item.htm
tech.root: mstv
ms.assetid: 9f7686d5-f454-46ea-ae50-5c140fda3099
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITuningSpaces interface [Microsoft TV Technologies],get_Item method, ITuningSpaces.get_Item, ITuningSpaces::get_Item, ITuningSpacesget_Item, get_Item, get_Item method [Microsoft TV Technologies], get_Item method [Microsoft TV Technologies],ITuningSpaces interface, mstv.ituningspaces_get_item, tuner/ITuningSpaces::get_Item
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - COM
api_location:
 - tuner.h
api_name:
 - ITuningSpaces.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuningSpaces::get_Item


## -description



The <b>get_Item</b> method returns the specified item in the collection.




## -parameters




### -param varIndex [in]

<b>VARIANT</b> type that specifies the ID of the tuning space. The ID uniquely identifies the tuning space within the <b>SystemTuningSpaces</b> object.


### -param TuningSpace [out]

Address of a variable that receives a pointer to the tuning space's <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface. The caller must release the interface.


## -returns



Returns S_OK if successful.




## -see-also




<a href="https://msdn.microsoft.com/db252e22-8efe-4bfc-8fd3-2be7022bbbbd">ITuningSpaces Interface</a>
 

 

