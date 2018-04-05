---
UID: NF:searchapi.IUrlAccessor4.ShouldIndexItemContent
title: IUrlAccessor4::ShouldIndexItemContent method
author: windows-driver-content
description: Identifies whether the item's content should be indexed.
old-location: search\_search_IUrlAccessor4_ShouldIndexItemContent.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor4\shouldindexitemcontent.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IUrlAccessor4, IUrlAccessor4 interface [search], ShouldIndexItemContent method, IUrlAccessor4::ShouldIndexItemContent, ShouldIndexItemContent method [search], ShouldIndexItemContent method [search], IUrlAccessor4 interface, ShouldIndexItemContent,IUrlAccessor4.ShouldIndexItemContent, _search_IUrlAccessor4_ShouldIndexItemContent, search._search_IUrlAccessor4_ShouldIndexItemContent, searchapi/IUrlAccessor4::ShouldIndexItemContent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Urlaccsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	IUrlAccessor4.ShouldIndexItemContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IUrlAccessor4::ShouldIndexItemContent method


## -description



            Identifies whether the item's content should be indexed. 
        


## -parameters




### -param pfIndexContent [out]

Type: <b>BOOL*</b>


                    A pointer to a <b>BOOL</b> value that indicates whether the item's content should be indexed.
                


## -returns



Type: <b>HRESULT</b>

Returns S_FALSE if the item's content should not be indexed.



