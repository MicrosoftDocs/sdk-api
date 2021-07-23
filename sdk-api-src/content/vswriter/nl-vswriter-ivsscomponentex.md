---
UID: NL:vswriter.IVssComponentEx
title: IVssComponentEx (vswriter.h)
description: Defines additional methods for examining and modifying information about components contained in a requester's Backup Components Document.
helpviewer_keywords: ["IVssComponentEx","IVssComponentEx interface","IVssComponentEx interface","described","base.ivsscomponentex","vswriter/IVssComponentEx"]
old-location: base\ivsscomponentex.htm
tech.root: base
ms.assetid: b11f65b0-2de2-478b-88b6-4696a8da2419
ms.date: 12/05/2018
ms.keywords: IVssComponentEx, IVssComponentEx interface, IVssComponentEx interface,described, base.ivsscomponentex, vswriter/IVssComponentEx
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssComponentEx
 - vswriter/IVssComponentEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssComponentEx
---

# IVssComponentEx class


## -description

Defines additional methods for examining  and modifying information about components contained in a requester's Backup 
    Components Document.

The <b>IVssComponentEx</b> interface is a C++ (not COM) interface.

To obtain an instance of the <b>IVssComponentEx</b> 
   interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a> interface, and pass 
   the <b>IID_IVssComponentEx</b> constant as the interface identifier (IID) parameter.

## -inheritance

The <b>IVssComponentEx</b> interface inherits from <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>. <b>IVssComponentEx</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>
