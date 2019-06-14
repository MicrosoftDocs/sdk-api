---
UID: NF:objidl.IStream.Stat
title: IStream::Stat (objidl.h)
author: windows-sdk-content
description: The Stat method retrieves the STATSTG structure for this stream.
old-location: stg\istream_stat.htm
tech.root: Stg
ms.assetid: c22ab396-dbc5-43a0-8448-35a2c094464f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStream interface [Structured Storage],Stat method, IStream.Stat, IStream::Stat, Stat, Stat method [Structured Storage], Stat method [Structured Storage],IStream interface, _stg_istream_stat, objidl/IStream::Stat, stg.istream_stat
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
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
 - IStream.Stat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStream::Stat


## -description


The <b>Stat</b> method retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstatstg">STATSTG</a> structure for this stream.


## -parameters




### -param pstatstg [out]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstatstg">STATSTG</a> structure where this method places information about this stream object.


### -param grfStatFlag [in]

Specifies that this method does not return some of the members in the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstatstg">STATSTG</a> structure, thus saving a memory allocation operation. Values are taken from the 
<a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ne-wtypes-tagstatflag">STATFLAG</a> enumeration.


## -returns



This method can return one of these values.




## -remarks



<b>IStream::Stat</b> retrieves a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstatstg">STATSTG</a> structure that contains information about this open stream. When this stream is within a structured storage and 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-enumelements">IStorage::EnumElements</a> is called, it creates an enumerator object with the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG</a> interface on it, which can be called to enumerate the storages and streams through the 
<b>STATSTG</b> structures associated with each of them.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ne-wtypes-tagstatflag">STATFLAG</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstatstg">STATSTG</a>
 

 

