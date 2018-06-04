---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# WS_XML_CANONICALIZATION_PROPERTY_ID enumeration


## -description


Identifies each XML canonicalization property and its associated
        value.  This enumeration is used within the <a href="https://msdn.microsoft.com/79f65ff2-4fa2-4808-b5cb-ad3aa6200260">WS_XML_CANONICALIZATION_PROPERTY</a> structure, which is used as a parameter to <a href="https://msdn.microsoft.com/5dad9485-db3c-4ae0-b053-e1e4f32ad64d">WsStartReaderCanonicalization</a> and <a href="https://msdn.microsoft.com/e9ea26d6-a136-4103-ac67-42e943ea67b5">WsStartWriterCanonicalization</a>.
      


## -enum-fields




### -field WS_XML_CANONICALIZATION_PROPERTY_ALGORITHM

A <a href="https://msdn.microsoft.com/230e4b9d-f6ce-45a8-9efd-2a6949d3e6f4">WS_XML_CANONICALIZATION_ALGORITHM</a> value that specifies the algorithm to be used for canonicalization.  If this is not specified,
          the <b>WS_EXCLUSIVE_XML_CANONICALIZATION_ALGORITHM</b> is used.
        


### -field WS_XML_CANONICALIZATION_PROPERTY_INCLUSIVE_PREFIXES

A <a href="https://msdn.microsoft.com/792ab726-6309-4f77-b40c-95dad2d991d9">WS_XML_CANONICALIZATION_INCLUSIVE_PREFIXES</a> structure that contains the set of prefixes to be treated as inclusive prefixes when using
          the exclusive canonicalization algorithm.  If this is not specified,
          no prefix is treated as an inclusive prefix.
        


### -field WS_XML_CANONICALIZATION_PROPERTY_OMITTED_ELEMENT

A <a href="https://msdn.microsoft.com/54095ad5-e9ba-4fa8-92e2-87b3a8950d5c">WS_XML_QNAME</a> structure that contains the elements to be omitted during canonicalization.  If one or more
          elements in the XML input match the specified name and namespace, then
          all such elements and the subtrees rooted at them are omitted from the
          canonical output.  This property can be used to implement enveloped
          signatures where canonicalization needs to skip a signature element
          that is embedded within the XML content being canonicalized and
          signed.  If this is not specified, no element is omitted from the
          output.
        


### -field WS_XML_CANONICALIZATION_PROPERTY_OUTPUT_BUFFER_SIZE

A <b>ULONG</b> that specifies the size of the buffer in which canonical bytes are accumulated.  Once at least this
          many bytes are generated, or canonicalization is ended by a call to <a href="https://msdn.microsoft.com/5cacad47-8581-4713-96cb-3b3a863e6327">WsEndReaderCanonicalization</a>
          or <a href="https://msdn.microsoft.com/169f971e-0cd2-44e7-81fc-059cc3cd357d">WsEndWriterCanonicalization</a>, the canonical bytes are
          written to the output specified at the start of canonicalization.  If this is
          not specified, a default buffer size of 1024 is used.

