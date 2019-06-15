---
UID: NN:shobjidl_core.IDestinationStreamFactory
title: IDestinationStreamFactory (shobjidl_core.h)
author: windows-sdk-content
description: Exposes a method for manually copying a stream or file before applying changes to properties.
old-location: shell\IDestinationStreamFactory.htm
tech.root: shell
ms.assetid: 7cedf8eb-b4ef-4889-bd7b-a734e939e872
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDestinationStreamFactory, IDestinationStreamFactory interface [Windows Shell], IDestinationStreamFactory interface [Windows Shell],described, shell.IDestinationStreamFactory, shell_IDestinationStreamFactory, shobjidl_core/IDestinationStreamFactory
ms.topic: interface
f1_keywords: ["shobjidl_core/IDestinationStreamFactory"]
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
ms.custom: 19H1
---

# IDestinationStreamFactory interface


## -description


Exposes a method for manually copying a stream or file before applying changes to properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDestinationStreamFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDestinationStreamFactory</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream">GetDestinationStream</a>
</td>
<td align="left" width="63%">
Gets an empty stream that receives the new version of the file being copied.

</td>
</tr>
</table> 


## -remarks



The default copy-on-write behavior provided by <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> causes the entire source stream to be duplicated during a write operation. This can be costly for large streams, especially when a large portion of the stream is to be changed. <b>IDestinationStreamFactory</b> provides an alternative for the property handler author, who can use it manually to ensure that property changes do not corrupt the stream in case of failure. To do this, the author marks the handler as NoTransactedMode in the handler's CoClass registry key, and queries the stream for this interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/properties/building-property-handlers-property-handlers">Initializing Property Handlers</a>
 

 

