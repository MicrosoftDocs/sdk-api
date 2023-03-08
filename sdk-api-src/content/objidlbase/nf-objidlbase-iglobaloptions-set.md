---
UID: NF:objidlbase.IGlobalOptions.Set
title: IGlobalOptions::Set (objidlbase.h)
description: The IGlobalOptions::Set (objidlbase.h) method sets the specified global property of the COM runtime.
helpviewer_keywords: ["IGlobalOptions interface [COM]","Set method","IGlobalOptions.Set","IGlobalOptions::Set","Set","Set method [COM]","Set method [COM]","IGlobalOptions interface","_com_iglobaloptions_set","com.iglobaloptions_set","objidlbase/IGlobalOptions::Set"]
old-location: com\iglobaloptions_set.htm
tech.root: com
ms.assetid: 5a59c862-64a4-45b5-8b6b-dacbfb4d170b
ms.date: 08/13/2022
ms.keywords: IGlobalOptions interface [COM],Set method, IGlobalOptions.Set, IGlobalOptions::Set, Set, Set method [COM], Set method [COM],IGlobalOptions interface, _com_iglobaloptions_set, com.iglobaloptions_set, objidlbase/IGlobalOptions::Set
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IGlobalOptions::Set
 - objidlbase/IGlobalOptions::Set
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IGlobalOptions.Set
---

# IGlobalOptions::Set


## -description

Sets the specified global property of the COM runtime.

## -parameters

### -param dwProperty [in]

 The global property of the COM runtime. For a list of properties that can be set with this method, see <a href="/windows/desktop/api/objidl/nn-objidl-iglobaloptions">IGlobalOptions</a>.

### -param dwValue [in]

The value of the property.<div class="alert"><b>Important</b>  For the COMGLB_APPID property, this parameter must specify a pointer to the APPID GUID.</div>
<div> </div>

## -returns

The return value is S_OK if the property was set successfully.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iglobaloptions">IGlobalOptions</a>
