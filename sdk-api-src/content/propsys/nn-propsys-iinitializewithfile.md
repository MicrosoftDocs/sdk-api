---
UID: NN:propsys.IInitializeWithFile
title: IInitializeWithFile (propsys.h)

description: Exposes a method to initialize a handler, such as a property handler, thumbnail handler, or preview handler, with a file path.
old-location: shell\IInitializeWithFile.htm
tech.root: shell
ms.assetid: 323181ab-1dc2-4b2a-a91f-3eccd7968bcd

ms.date: 12/05/2018
ms.keywords: IInitializeWithFile, IInitializeWithFile interface [Windows Shell], IInitializeWithFile interface [Windows Shell],described, propsys/IInitializeWithFile, shell.IInitializeWithFile, shell_IInitializeWithFile
ms.topic: interface
f1_keywords: 
 - "propsys/IInitializeWithFile"
dev_langs:
 - c++
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - Propsys.h
api_name:
 - IInitializeWithFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInitializeWithFile interface


## -description


Exposes a method to initialize a handler, such as a property handler, thumbnail handler, or preview handler, with a file path.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitializeWithFile</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInitializeWithFile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInitializeWithFile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-iinitializewithfile-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a handler with a file path.

</td>
</tr>
</table> 


## -remarks



Whenever possible, it is recommended that initialization be done through a stream using <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-iinitializewithstream">IInitializeWithStream</a>. Benefits of this include increased security and stability.



