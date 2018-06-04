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

# IShellItem::GetAttributes


## -description


Gets a requested set of attributes of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object.


## -parameters




### -param sfgaoMask [in]

Type: <b>SFGAOF</b>

Specifies the attributes to retrieve. One or more of the <a href="https://msdn.microsoft.com/4cb85995-cdc8-4474-8c4d-c783ac91c759">SFGAO</a> values. Use a bitwise OR operator to determine the attributes to retrieve.


### -param psfgaoAttribs [out]

Type: <b>SFGAOF*</b>

A pointer to a value that, when this method returns successfully, contains the requested attributes. One or more of the <a href="https://msdn.microsoft.com/4cb85995-cdc8-4474-8c4d-c783ac91c759">SFGAO</a> values. Only those attributes specified by <i>sfgaoMask</i> are returned; other attribute values are undefined.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the attributes returned exactly match those requested in <i>sfgaoMask</i>, S_FALSE if the attributes do not exactly match, or a standard COM error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/0498ce03-9949-48bb-a1eb-b569f4171884">GetAttributes</a>



<a href="https://msdn.microsoft.com/3864b386-7653-4661-880c-e96c08ff0dbb">GetAttributesOf</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

