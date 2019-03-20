---
UID: NF:mpeg2data.IMpeg2TableFilter.AddTable
title: IMpeg2TableFilter::AddTable (mpeg2data.h)
author: windows-sdk-content
description: The AddTable method adds a table identifier (TID) to the list of MPEG-2 table sections that the filter sends.
old-location: mstv\impeg2tablefilter_addtable.htm
tech.root: mstv
ms.assetid: b789bfda-bb7e-4a7b-999e-0e2e798df4d5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddTable, AddTable method [Microsoft TV Technologies], AddTable method [Microsoft TV Technologies],IMpeg2TableFilter interface, IMpeg2TableFilter interface [Microsoft TV Technologies],AddTable method, IMpeg2TableFilter.AddTable, IMpeg2TableFilter::AddTable, IMpeg2TableFilterAddTable, mpeg2data/IMpeg2TableFilter::AddTable, mstv.impeg2tablefilter_addtable
ms.topic: method
req.header: mpeg2data.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - IMpeg2TableFilter.AddTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMpeg2TableFilter::AddTable


## -description



The <b>AddTable</b> method adds a table identifier (TID) to the list of MPEG-2 table sections that the filter sends.




## -parameters




### -param p [in]

Specifies the packet identifier (PID) of the transport stream packets to examine.


### -param t [in]

Specifies the TID of the section to retrieve.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/9467352d-44a5-41eb-b426-28df83a6d423">IMpeg2TableFilter Interface</a>
 

 

