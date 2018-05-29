---
UID: NF:objidl.IStream.Stat
title: IStream::Stat
author: windows-sdk-content
description: The Stat method retrieves the STATSTG structure for this stream.
old-location: stg\istream_stat.htm
old-project: Stg
ms.assetid: c22ab396-dbc5-43a0-8448-35a2c094464f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IStream interface [Structured Storage],Stat method, IStream.Stat, IStream::Stat, Stat, Stat method [Structured Storage], Stat method [Structured Storage],IStream interface, _stg_istream_stat, objidl/IStream::Stat, stg.istream_stat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IStream.Stat
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStream::Stat


## -description



			The <b>Stat</b> method retrieves the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure for this stream.


## -parameters




### -param pstatstg [out]

Pointer to a 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure where this method places information about this stream object.


### -param grfStatFlag [in]

Specifies that this method does not return some of the members in the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure, thus saving a memory allocation operation. Values are taken from the 
<a href="https://msdn.microsoft.com/9070b517-8ca5-455f-baee-0647b1895c08">STATFLAG</a> enumeration.


## -returns



This method can return one of these values.




## -remarks



<b>IStream::Stat</b> retrieves a pointer to the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure that contains information about this open stream. When this stream is within a structured storage and 
<a href="https://msdn.microsoft.com/29ca157e-40e2-4e9a-95fb-a31bb45570f2">IStorage::EnumElements</a> is called, it creates an enumerator object with the 
<a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a> interface on it, which can be called to enumerate the storages and streams through the 
<b>STATSTG</b> structures associated with each of them.




## -see-also




<a href="https://msdn.microsoft.com/52474e37-0e14-4dcc-8e04-4442cfd26eb3">IStream - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/9070b517-8ca5-455f-baee-0647b1895c08">STATFLAG</a>



<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a>
 

 

