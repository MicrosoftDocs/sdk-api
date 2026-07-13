---
UID: NF:xpsobjectmodel.IXpsOMDictionary.GetByKey
title: IXpsOMDictionary::GetByKey (xpsobjectmodel.h)
description: Gets the IXpsOMShareable interface pointer of the entry that contains the specified key.
helpviewer_keywords: ["GetByKey","GetByKey method [XPS Documents and Packaging]","GetByKey method [XPS Documents and Packaging]","IXpsOMDictionary interface","IXpsOMDictionary interface [XPS Documents and Packaging]","GetByKey method","IXpsOMDictionary.GetByKey","IXpsOMDictionary::GetByKey","xps.ixpsomdictionary_getbykey","xpsobjectmodel/IXpsOMDictionary::GetByKey"]
old-location: xps\ixpsomdictionary_getbykey.htm
tech.root: xps
ms.assetid: 6efc2fed-e372-4416-9645-50c1430f0e75
ms.date: 12/05/2018
ms.keywords: GetByKey, GetByKey method [XPS Documents and Packaging], GetByKey method [XPS Documents and Packaging],IXpsOMDictionary interface, IXpsOMDictionary interface [XPS Documents and Packaging],GetByKey method, IXpsOMDictionary.GetByKey, IXpsOMDictionary::GetByKey, xps.ixpsomdictionary_getbykey, xpsobjectmodel/IXpsOMDictionary::GetByKey
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - IXpsOMDictionary::GetByKey
 - xpsobjectmodel/IXpsOMDictionary::GetByKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMDictionary.GetByKey
---

# IXpsOMDictionary::GetByKey


## -description

Gets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface pointer of the entry that contains the specified key.

## -parameters

### -param key [in]

The entry's key to be found in the dictionary.

### -param beforeEntry [in]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface pointer to the last entry in the dictionary which is to be searched for <i>key</i>. If <i>beforeEntry</i> is <b>NULL</b> or is an interface pointer to an entry that is not in the dictionary, the entire dictionary will be searched.

### -param entry [out, retval]

The interface pointer to the dictionary entry whose key matches <i>key</i>.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The interface pointers stored in a dictionary will usually point to interfaces, such as  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>                 and <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>, that are derived from the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface. To determine the interface type, call the <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomshareable-gettype">IXpsOMShareable::GetType</a> method.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>