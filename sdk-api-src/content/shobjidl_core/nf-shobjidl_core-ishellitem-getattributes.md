---
UID: NF:shobjidl_core.IShellItem.GetAttributes
title: IShellItem::GetAttributes
author: windows-sdk-content
description: Gets a requested set of attributes of the IShellItem object.
old-location: shell\IShellItem_GetAttributes.htm
tech.root: shell
ms.assetid: d8d48b4b-979e-48ed-9e57-279fd6fad5cc
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetAttributes, GetAttributes method [Windows Shell], GetAttributes method [Windows Shell],IShellItem interface, IShellItem interface [Windows Shell],GetAttributes method, IShellItem.GetAttributes, IShellItem::GetAttributes, _win32_IShellItem_GetAttributes, shell.IShellItem_GetAttributes, shobjidl_core/IShellItem::GetAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellItem.GetAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

