---
UID: NN:shobjidl_core.IDestinationStreamFactory
title: IDestinationStreamFactory
author: windows-sdk-content
description: Exposes a method for manually copying a stream or file before applying changes to properties.
old-location: shell\IDestinationStreamFactory.htm
tech.root: shell
ms.assetid: 7cedf8eb-b4ef-4889-bd7b-a734e939e872
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IDestinationStreamFactory, IDestinationStreamFactory interface [Windows Shell], IDestinationStreamFactory interface [Windows Shell],described, shell.IDestinationStreamFactory, shell_IDestinationStreamFactory, shobjidl_core/IDestinationStreamFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDestinationStreamFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDestinationStreamFactory interface


## -description


Exposes a method for manually copying a stream or file before applying changes to properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDestinationStreamFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDestinationStreamFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDestinationStreamFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4903a3a1-12b7-4094-aac8-6e8525998c3c">GetDestinationStream</a>
</td>
<td align="left" width="63%">
Gets an empty stream that receives the new version of the file being copied.

</td>
</tr>
</table> 


## -remarks



The default copy-on-write behavior provided by <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> causes the entire source stream to be duplicated during a write operation. This can be costly for large streams, especially when a large portion of the stream is to be changed. <b>IDestinationStreamFactory</b> provides an alternative for the property handler author, who can use it manually to ensure that property changes do not corrupt the stream in case of failure. To do this, the author marks the handler as NoTransactedMode in the handler's CoClass registry key, and queries the stream for this interface.




## -see-also




<a href="https://msdn.microsoft.com/3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9">Initializing Property Handlers</a>
 

 

