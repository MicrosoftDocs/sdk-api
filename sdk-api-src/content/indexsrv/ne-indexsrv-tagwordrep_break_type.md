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

# tagWORDREP_BREAK_TYPE enumeration


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Describes the type of break that separates the current word from the previous word.


## -enum-fields




### -field WORDREP_BREAK_EOW

A word break is placed between this word and the previous word that was placed in the <b>WordSink</b>. This break is the default used by the <a href="https://msdn.microsoft.com/3de6e9a7-2213-4401-84a2-7fa73c9d5547">PutWord</a> method.


### -field WORDREP_BREAK_EOS

A sentence break is placed between this word and the previous word.


### -field WORDREP_BREAK_EOP

A paragraph break is placed between this word and the previous word. 


### -field WORDREP_BREAK_EOC

A chapter break is placed between this word and the previous word.


## -see-also




<a href="https://msdn.microsoft.com/6e0d0ec1-1ab9-4cbf-bb28-e38aaa42f41e">IWordSink::PutAltWord</a>



<a href="https://msdn.microsoft.com/3de6e9a7-2213-4401-84a2-7fa73c9d5547">IWordSink::PutWord</a>
 

 

