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

# IWSManResourceLocator::get_FragmentDialect


## -description


Gets or sets the language dialect for a <a href="windows_remote_management_glossary.htm">resource</a> <a href="windows_remote_management_glossary.htm">fragment</a> <i>dialect</i> when <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> is used in <a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a> object methods such as <a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>, <a href="https://msdn.microsoft.com/1224dab8-82d1-4416-8c21-e84fdda15deb">Put</a>, or <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">Enumerate</a>. A fragment represents one property or part of a resource. You can provide an <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> object instead of specifying a <a href="windows_remote_management_glossary.htm">resource URI</a> in <a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a> object operations. 

This property is read/write.


## -parameters


## -remarks



The dialect string defaults to the XPath 1.0 specification. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84163">http://www.w3.org/TR/xpath</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a>



<a href="https://msdn.microsoft.com/60b08084-f4b9-4049-b0cd-a7420fcffd7c">ResourceLocator.FragmentDialect</a>
 

 

