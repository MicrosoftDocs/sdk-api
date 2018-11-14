---
UID: NF:mpeg2data.IMpeg2TableFilter.AddExtension
title: IMpeg2TableFilter::AddExtension
author: windows-sdk-content
description: The AddExtension method adds a table extension to the list of MPEG-2 table sections that the filter sends.
old-location: mstv\impeg2tablefilter_addextension.htm
tech.root: MSTV
ms.assetid: 20484b0e-c6c8-4741-9672-a991ba368e92
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddExtension, AddExtension method [Microsoft TV Technologies], AddExtension method [Microsoft TV Technologies],IMpeg2TableFilter interface, IMpeg2TableFilter interface [Microsoft TV Technologies],AddExtension method, IMpeg2TableFilter.AddExtension, IMpeg2TableFilter::AddExtension, IMpeg2TableFilterAddExtension, mpeg2data/IMpeg2TableFilter::AddExtension, mstv.impeg2tablefilter_addextension
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMpeg2TableFilter.AddExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mpeg2data.h
: 
- IMpeg2TableFilter.AddExtension
: 
---

# IMpeg2TableFilter::AddExtension


## -description



The <b>AddExtension</b> method adds a table extension to the list of MPEG-2 table sections that the filter sends.




## -parameters




### -param p [in]

Specifies the packet identifier (PID) of the transport stream packets to examine.


### -param t [in]

Specifies the table identifier (TID) of the section to retrieve.


### -param e [in]

Specifies the table_extension identifier of the section to retrieve.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/9467352d-44a5-41eb-b426-28df83a6d423">IMpeg2TableFilter Interface</a>
 

 

