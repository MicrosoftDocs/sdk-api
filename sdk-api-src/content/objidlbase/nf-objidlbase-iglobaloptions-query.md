---
UID: NF:objidlbase.IGlobalOptions.Query
title: IGlobalOptions::Query
author: windows-sdk-content
description: Queries the specified global property of the COM runtime.
old-location: com\iglobaloptions_query.htm
tech.root: com
ms.assetid: ee16e59d-c629-45c1-afe6-fb4e37eba5d1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IGlobalOptions interface [COM],Query method, IGlobalOptions.Query, IGlobalOptions::Query, Query, Query method [COM], Query method [COM],IGlobalOptions interface, _com_iglobaloptions_query, com.iglobaloptions_query, objidlbase/IGlobalOptions::Query
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IGlobalOptions.Query
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- objidlbase.h
: 
- IGlobalOptions.Query
: 
---

# IGlobalOptions::Query


## -description


Queries the specified global property of the COM runtime.


## -parameters




### -param dwProperty [in]

 The global property of the COM runtime. For a list of properties that can be set with this method, see <a href="https://msdn.microsoft.com/c5e823be-521d-4eb4-8836-fdd2cac6f15d">IGlobalOptions</a>.


### -param pdwValue [out]

The value of the property.<div class="alert"><b>Important</b>  For the COMGLB_APPID property, this parameter receives a pointer to the AppID GUID.</div>
<div> </div>



## -returns



The return value is S_OK if the property is queried successfully.




## -see-also




<a href="https://msdn.microsoft.com/c5e823be-521d-4eb4-8836-fdd2cac6f15d">IGlobalOptions</a>
 

 

