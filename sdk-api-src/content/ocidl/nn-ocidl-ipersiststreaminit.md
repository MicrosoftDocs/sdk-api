---
UID: NN:ocidl.IPersistStreamInit
title: IPersistStreamInit (ocidl.h)
description: A replacement for IPersistStream that adds an initialization method.
helpviewer_keywords: ["IPersistStreamInit","IPersistStreamInit interface [COM]","IPersistStreamInit interface [COM]","described","_com_ipersiststreaminit","com.ipersiststreaminit","ocidl/IPersistStreamInit"]
old-location: com\ipersiststreaminit.htm
tech.root: com
ms.assetid: 49c413b3-3523-4602-9ec1-19f4e0fe5651
ms.date: 12/05/2018
ms.keywords: IPersistStreamInit, IPersistStreamInit interface [COM], IPersistStreamInit interface [COM],described, _com_ipersiststreaminit, com.ipersiststreaminit, ocidl/IPersistStreamInit
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistStreamInit
 - ocidl/IPersistStreamInit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPersistStreamInit
---

# IPersistStreamInit interface


## -description

A replacement for <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> that adds an initialization method.

This interface is not derived from <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>; it is mutually exclusive with <b>IPersistStream</b>. An object chooses to support only one of the two interfaces, based on whether it requires the <a href="/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew">InitNew</a> method.

## -inheritance

The <b>IPersistStreamInit</b> interface inherits from <b>IPersist</b>. <b>IPersistStreamInit</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>
