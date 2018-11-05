---
UID: NF:clusapi.ALIGN_CLUSPROP
title: ALIGN_CLUSPROP macro
author: windows-sdk-content
description: Aligns structures properly within value lists.
old-location: mscs\align_clusprop.htm
tech.root: mscs
ms.assetid: af7c9d39-b76f-494d-af5d-7e0baf0ace2d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ALIGN_CLUSPROP, ALIGN_CLUSPROP macro [Failover Cluster], _wolf_align_clusprop, clusapi/ALIGN_CLUSPROP, mscs.align_clusprop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - ClusAPI.h
api_name:
 - ALIGN_CLUSPROP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ALIGN_CLUSPROP macro


## -description


Aligns structures properly within  <a href="https://msdn.microsoft.com/en-us/library/Aa373112(v=VS.85).aspx">value lists</a>.


## -parameters




### -param count

Size, in bytes, of the data to align. This value must be a constant.


## -remarks



<b>ALIGN_CLUSPROP</b> returns a value that is greater than or equal to <i>count</i>. The value represents the total byte size of the data plus the padding required for proper alignment.

ClusAPI.h defines  <b>ALIGN_CLUSPROP</b> as follows:

<code>#define ALIGN_CLUSPROP( count ) ((count + 3) &amp; ~3)</code>


#### Examples

The following example illustrates how to use  <b>ALIGN_CLUSPROP</b> to calculate the size of a value list entry. For additional examples, see  <a href="https://msdn.microsoft.com/en-us/library/Aa372958(v=VS.85).aspx">Using Lists and Tables</a>.


```cpp
WCHAR szData[] = L"StringData";
DWORD cbSizeofValueListEntry;

cbSizeofValueListEntry = sizeof( CLUSPROP_VALUE ) + 
                         ALIGN_CLUSPROP( sizeof( szData ) );

```




