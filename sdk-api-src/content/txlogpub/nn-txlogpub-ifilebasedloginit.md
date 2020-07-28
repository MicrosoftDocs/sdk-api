---
UID: NN:txlogpub.IFileBasedLogInit
title: IFileBasedLogInit (txlogpub.h)
description: Initializes an instance of a file based implementation of ILog.
helpviewer_keywords: ["IFileBasedLogInit","IFileBasedLogInit interface [COM]","IFileBasedLogInit interface [COM]","described","_com_ifilebasedloginit","com.ifilebasedloginit","txlogpub/IFileBasedLogInit"]
old-location: com\ifilebasedloginit.htm
tech.root: com
ms.assetid: c499f32b-3897-4c61-b9c1-d660648aab76
ms.date: 12/05/2018
ms.keywords: IFileBasedLogInit, IFileBasedLogInit interface [COM], IFileBasedLogInit interface [COM],described, _com_ifilebasedloginit, com.ifilebasedloginit, txlogpub/IFileBasedLogInit
f1_keywords:
- txlogpub/IFileBasedLogInit
dev_langs:
- c++
req.header: txlogpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Txlogpub.idl
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
- Txlogpub.h
api_name:
- IFileBasedLogInit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileBasedLogInit interface


## -description


Initializes an instance of a file based implementation of <a href="https://docs.microsoft.com/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileBasedLogInit</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileBasedLogInit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileBasedLogInit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/txlogpub/nf-txlogpub-ifilebasedloginit-initnew">InitNew</a>
</td>
<td align="left" width="63%">
Create a new log instance on the specified file.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a>
 

 

