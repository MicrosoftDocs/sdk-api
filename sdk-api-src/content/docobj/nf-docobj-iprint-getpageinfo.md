---
UID: NF:docobj.IPrint.GetPageInfo
title: IPrint::GetPageInfo
author: windows-sdk-content
description: Retrieves the number of a document's first page and the total number of pages.
old-location: com\iprint_getpageinfo.htm
old-project: com
ms.assetid: 8f3a2d21-5345-4c4e-9928-37dcd6ec5fcc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPageInfo, GetPageInfo method [COM], GetPageInfo method [COM],IPrint interface, IPrint interface [COM],GetPageInfo method, IPrint.GetPageInfo, IPrint::GetPageInfo, _ctrl_iprint_getpageinfo, com.iprint_getpageinfo, docobj/IPrint::GetPageInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: docobj.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DOCMISC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IPrint.GetPageInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPrint::GetPageInfo


## -description


Retrieves the number of a document's first page and the total number of pages.


## -parameters




### -param pnFirstPage [out]

A pointer to a variable that receives the page number of the first page. This parameter can be <b>NULL</b>, indicating that the caller is not interested in this number. If <a href="https://msdn.microsoft.com/352a4dc0-c79e-46e3-8212-55fd7d2916bc">IPrint::SetInitialPageNum</a> has been called, this parameter should contain the same value passed to that method. Otherwise, the value is the document's internal first page number.


### -param pcPages [out]

A pointer to a variable that receives the total number of pages in this document. This parameter can be <b>NULL</b>, indicating that the caller is not interested in this number.


## -returns



This method can return the standard return values E_UNEXPECTED and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/eb0d15c0-8a34-4211-b840-29d5862cf767">IPrint</a>
 

 

