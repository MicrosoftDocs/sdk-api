---
UID: NF:objidl.IGlobalOptions.Query
title: IGlobalOptions::Query (objidl.h)
description: The IGlobalOptions::Query method (objidl.h) queries the specified global property of the COM runtime.
helpviewer_keywords: ["IGlobalOptions interface [COM]","Query method","IGlobalOptions.Query","IGlobalOptions::Query","Query","Query method [COM]","Query method [COM]","IGlobalOptions interface","_com_iglobaloptions_query","com.iglobaloptions_query","objidlbase/IGlobalOptions::Query"]
old-location: com\iglobaloptions_query.htm
tech.root: com
ms.assetid: ee16e59d-c629-45c1-afe6-fb4e37eba5d1
ms.date: 08/12/2022
ms.keywords: IGlobalOptions interface [COM],Query method, IGlobalOptions.Query, IGlobalOptions::Query, Query, Query method [COM], Query method [COM],IGlobalOptions interface, _com_iglobaloptions_query, com.iglobaloptions_query, objidlbase/IGlobalOptions::Query
req.header: objidl.h
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
 - IGlobalOptions::Query
 - objidl/IGlobalOptions::Query
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
 - IGlobalOptions.Query
---

# IGlobalOptions::Query


## -description

Queries the specified global property of the COM runtime.

## -parameters

### -param dwProperty [in]

 The global property of the COM runtime. For a list of properties that can be set with this method, see <a href="/windows/desktop/api/objidl/nn-objidl-iglobaloptions">IGlobalOptions</a>.

### -param pdwValue [out]

The value of the property.<div class="alert"><b>Important</b>  For the COMGLB_APPID property, this parameter receives a pointer to the AppID GUID.</div>
<div> </div>

## -returns

The return value is S_OK if the property is queried successfully.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iglobaloptions">IGlobalOptions</a>
