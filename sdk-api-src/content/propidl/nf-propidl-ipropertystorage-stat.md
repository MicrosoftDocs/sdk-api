---
UID: NF:propidl.IPropertyStorage.Stat
title: IPropertyStorage::Stat
author: windows-driver-content
description: The Stat method retrieves information about the current open property set.
old-location: stg\ipropertystorage_stat.htm
old-project: Stg
ms.assetid: 46985c49-cb9b-4f67-8dff-e6fad9e188da
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IPropertyStorage interface [Structured Storage],Stat method, IPropertyStorage.Stat, IPropertyStorage::Stat, Stat, Stat method [Structured Storage], Stat method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_stat, propidl/IPropertyStorage::Stat, stg.ipropertystorage_stat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propidl.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROFILEINFOW, *LPPROFILEINFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IPropertyStorage.Stat
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyStorage::Stat


## -description



			The <b>Stat</b> method retrieves information about the current open property set.


## -parameters




### -param pstatpsstg [out]

Pointer to a 
<a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structure, which contains statistics about the current open property set.


## -returns




						This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



<b>IPropertyStorage::Stat</b> fills in and returns a pointer to a 
<a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structure, containing statistics about the current property set.




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/979ee86b-fabc-428c-8134-f16c2a33270f">IPropertySetStorage::Enum</a>



<a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a>
 

 

