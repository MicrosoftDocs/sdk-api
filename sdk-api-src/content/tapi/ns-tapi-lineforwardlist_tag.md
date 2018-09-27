---
UID: NS:tapi.lineforwardlist_tag
title: lineforwardlist_tag
author: windows-sdk-content
description: The LINEFORWARDLIST structure describes a list of forwarding instructions. This structure can contain an array of LINEFORWARD structures. The lineForward and TSPI_lineForward functions use the LINEFORWARDLIST structure.
old-location: tapi2\lineforwardlist_str.htm
tech.root: tapi
ms.assetid: 3dec9ab6-43d8-4dda-b0b1-a25407e4d77a
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*LPLINEFORWARDLIST, LINEFORWARDLIST, LINEFORWARDLIST structure [TAPI 2.2], LPLINEFORWARDLIST, LPLINEFORWARDLIST structure pointer [TAPI 2.2], _tapi2_lineforwardlist_str, lineforwardlist_tag, tapi/LINEFORWARDLIST, tapi/LPLINEFORWARDLIST, tapi2.lineforwardlist_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
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
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEFORWARDLIST
product: Windows
targetos: Windows
req.typenames: LINEFORWARDLIST, *LPLINEFORWARDLIST
req.redist: 
---

# lineforwardlist_tag structure


## -description


The 
<b>LINEFORWARDLIST</b> structure describes a list of forwarding instructions. This structure can contain an array of 
<a href="https://msdn.microsoft.com/cbdb4409-a51a-4ddf-b3ec-c5b958fc2527">LINEFORWARD</a> structures. The 
<a href="https://msdn.microsoft.com/68dc99c5-1158-4e18-8e32-08216ff3567b">lineForward</a> and 
<a href="https://msdn.microsoft.com/fd70bf7f-653c-47db-bf81-6a620f47e5bc">TSPI_lineForward</a> functions use the 
<b>LINEFORWARDLIST</b> structure.


## -struct-fields




### -field dwTotalSize

Total size of the data structure, in bytes.


### -field dwNumEntries

Number of entries in the array specified as <b>ForwardList[]</b>.


### -field ForwardList

Array of forwarding instruction. The array's entries are of type 
<a href="https://msdn.microsoft.com/cbdb4409-a51a-4ddf-b3ec-c5b958fc2527">LINEFORWARD</a>.


## -remarks



This structure may not be extended.

The 
<b>LINEFORWARDLIST</b> structure defines the forwarding parameters requested for forwarding calls on an address or on all addresses on a line.




## -see-also




<a href="https://msdn.microsoft.com/cbdb4409-a51a-4ddf-b3ec-c5b958fc2527">LINEFORWARD</a>



<a href="https://msdn.microsoft.com/fd70bf7f-653c-47db-bf81-6a620f47e5bc">TSPI_lineForward</a>



<a href="https://msdn.microsoft.com/68dc99c5-1158-4e18-8e32-08216ff3567b">lineForward</a>
 

 

