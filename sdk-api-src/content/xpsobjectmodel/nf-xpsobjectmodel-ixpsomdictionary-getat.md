---
UID: NF:xpsobjectmodel.IXpsOMDictionary.GetAt
title: IXpsOMDictionary::GetAt (xpsobjectmodel.h)
description: Gets the IXpsOMShareable interface pointer and the key name string of the entry at a specified index in the dictionary.helpviewer_keywords: ["GetAt","GetAt method [XPS Documents and Packaging]","GetAt method [XPS Documents and Packaging]","IXpsOMDictionary interface","IXpsOMDictionary interface [XPS Documents and Packaging]","GetAt method","IXpsOMDictionary.GetAt","IXpsOMDictionary::GetAt","xps.ixpsomdictionary_getat","xpsobjectmodel/IXpsOMDictionary::GetAt"]
old-location: xps\ixpsomdictionary_getat.htm
tech.root: printdocs
ms.assetid: 818797dd-7255-453c-85b3-cf0c44fe5d0d
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMDictionary interface, IXpsOMDictionary interface [XPS Documents and Packaging],GetAt method, IXpsOMDictionary.GetAt, IXpsOMDictionary::GetAt, xps.ixpsomdictionary_getat, xpsobjectmodel/IXpsOMDictionary::GetAt
f1_keywords:
- xpsobjectmodel/IXpsOMDictionary.GetAt
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsobjectmodel.h
api_name:
- IXpsOMDictionary.GetAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMDictionary::GetAt


## -description


Gets the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface pointer and the key name string of the entry at a specified index in the dictionary.


## -parameters




### -param index [in]

The zero-based index of the dictionary entry that is to be obtained.


### -param key [out]

The key string that is found at the location specified by <i>index</i>.


### -param entry [out, retval]

The <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface pointer that is found at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The interface pointers that are stored in a dictionary will usually point to interfaces, such as <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>                 and <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>, that are derived from the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface. To determine the interface type, call the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomshareable-gettype">IXpsOMShareable::GetType</a> method.

This method allocates the memory used by the string that is returned in <i>key</i>.  If <i>key</i> is not <b>NULL</b>, use the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

