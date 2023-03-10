---
UID: NN:objidlbase.IMarshalingStream
title: IMarshalingStream (objidlbase.h)
description: The IMarshalingStream (objidlbase.h) interface provides additional information about the marshaling context to custom-marshaled objects and unmarshalers.
helpviewer_keywords: ["IMarshalingStream","IMarshalingStream interface [COM]","IMarshalingStream interface [COM]","described","com.imarshalingstream","objidl/IMarshalingStream"]
old-location: com\imarshalingstream.htm
tech.root: com
ms.assetid: 7C4A3982-3623-4F1F-929C-6D0503700450
ms.date: 08/15/2022
ms.keywords: IMarshalingStream, IMarshalingStream interface [COM], IMarshalingStream interface [COM],described, com.imarshalingstream, objidl/IMarshalingStream
req.header: objidlbase.h
req.include-header: Objidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
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
 - IMarshalingStream
 - objidlbase/IMarshalingStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidl.h
api_name:
 - IMarshalingStream
---

# IMarshalingStream interface


## -description

Provides additional information about the marshaling context to custom-marshaled objects and unmarshalers.

## -inheritance

The <b>IMarshalingStream</b> interface inherits from <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>. <b>IMarshalingStream</b> also has these types of members:

## -remarks

Implement <b>IMarshalingStream</b> interface if you have <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> implementations that call the marshaling APIs and provide the correct value of any of the attributes. This is essential only for <b>IStream</b> implementations that are used in hybrid policy processes.

## -see-also

<a href="/windows/win32/api/objidl/ne-objidl-globalopt_unmarshaling_policy_values">GLOBALOPT_UNMARSHALING_POLICY_VALUES</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>
