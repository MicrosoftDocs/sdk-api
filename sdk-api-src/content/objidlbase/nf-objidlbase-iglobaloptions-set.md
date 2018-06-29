---
UID: NF:objidlbase.IGlobalOptions.Set
title: IGlobalOptions::Set
author: windows-sdk-content
description: Sets the specified global property of the COM runtime.
old-location: com\iglobaloptions_set.htm
old-project: com
ms.assetid: 5a59c862-64a4-45b5-8b6b-dacbfb4d170b
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IGlobalOptions interface [COM],Set method, IGlobalOptions.Set, IGlobalOptions::Set, Set, Set method [COM], Set method [COM],IGlobalOptions interface, _com_iglobaloptions_set, com.iglobaloptions_set, objidlbase/IGlobalOptions::Set
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IGlobalOptions.Set
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IGlobalOptions::Set


## -description


Sets the specified global property of the COM runtime.


## -parameters




### -param dwProperty [in]

 The global property of the COM runtime. For a list of properties that can be set with this method, see <a href="https://msdn.microsoft.com/c5e823be-521d-4eb4-8836-fdd2cac6f15d">IGlobalOptions</a>.


### -param dwValue [in]

The value of the property.<div class="alert"><b>Important</b>  For the COMGLB_APPID property, this parameter must specify a pointer to the APPID GUID.</div>
<div> </div>



## -returns



The return value is S_OK if the property was set successfully.




## -see-also




<a href="https://msdn.microsoft.com/c5e823be-521d-4eb4-8836-fdd2cac6f15d">IGlobalOptions</a>
 

 

