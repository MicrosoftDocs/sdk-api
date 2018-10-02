---
UID: NF:pla.IDataCollectorSet.SetValue
title: IDataCollectorSet::SetValue
author: windows-sdk-content
description: Sets a user-defined value.
old-location: pla\idatacollectorset_setvalue.htm
tech.root: PLA
ms.assetid: d2143de9-f189-47e0-8b28-0422d9984459
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDataCollectorSet interface [PLA],SetValue method, IDataCollectorSet.SetValue, IDataCollectorSet::SetValue, SetValue, SetValue method [PLA], SetValue method [PLA],IDataCollectorSet interface, base.idatacollectorset_setvalue, pla.idatacollectorset_setvalue, pla/IDataCollectorSet::SetValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
req.include-header: 
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
req.lib: 
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.SetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollectorSet::SetValue


## -description


Sets a user-defined value.


## -parameters




### -param key

TBD


### -param value

TBD




#### - Key [in]

The name of the value. 


#### - pValue [in]

The value associated with the key. 


## -returns



Returns S_OK if successful.




## -remarks



You can specify one or more user-defined values. If you specify a key that currently exists, the current value is overwritten. To remove a value, set the <i>pValue</i> parameter to <b>NULL</b>.

You use the key value if you want to perform variable substitution in the <a href="https://msdn.microsoft.com/7bd045df-379b-40fb-b309-cec531493018">IDataCollectorSet::TaskArguments</a> property.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/0f82e154-7d3f-44c9-8bdd-cc1522499e85">IDataCollectorSet::GetValue</a>
 

 

