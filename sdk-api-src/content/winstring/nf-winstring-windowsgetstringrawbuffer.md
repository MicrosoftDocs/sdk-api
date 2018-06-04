---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WindowsGetStringRawBuffer function


## -description


Gets the backing buffer for the specified string.


## -parameters




### -param string [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The string for which the backing buffer is to be retrieved.


### -param length [out, optional]

Type: <b>UINT32*</b>

The number of Unicode characters in the backing buffer for <i>string</i>, including embedded null characters, but excluding the terminating null; or 0 if <i>string</i> is <b>NULL</b>.


## -returns



Type: <b>PCWSTR</b>

A pointer to the buffer that provides the backing store for <i>string</i>, or the empty string if  <i>string</i> is <b>NULL</b> or the empty string.




## -remarks



Use the <b>WindowsGetStringRawBuffer</b>  function to obtain a pointer to the backing buffer of  an <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>.

Do not change the contents of the buffer as all  <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRINGs</a> are required to be immutable.



