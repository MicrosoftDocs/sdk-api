---
UID: NF:propidlbase.IPropertyStorage.Stat
title: IPropertyStorage::Stat (propidlbase.h)
author: windows-sdk-content
description: The Stat method retrieves information about the current open property set.
old-location: stg\ipropertystorage_stat.htm
tech.root: Stg
ms.assetid: 46985c49-cb9b-4f67-8dff-e6fad9e188da
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPropertyStorage interface [Structured Storage],Stat method, IPropertyStorage.Stat, IPropertyStorage::Stat, Stat, Stat method [Structured Storage], Stat method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_stat, propidl/IPropertyStorage::Stat, stg.ipropertystorage_stat
ms.topic: method
f1_keywords: 
 - "propidlbase/IPropertyStorage.Stat"
req.header: propidlbase.h
req.include-header: Objbase.h, Propidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IPropertyStorage.Stat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyStorage::Stat


## -description


The <b>Stat</b> method retrieves information about the current open property set.


## -parameters




### -param pstatpsstg [out]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structure, which contains statistics about the current open property set.


## -returns



This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



<b>IPropertyStorage::Stat</b> fills in and returns a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structure, containing statistics about the current property set.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-enum">IPropertySetStorage::Enum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a>
 

 

