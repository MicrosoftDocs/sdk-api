---
UID: NF:shobjidl_core.IEnumObjects.Next
title: IEnumObjects::Next
author: windows-sdk-content
description: Gets the next specified number and type of objects.
old-location: shell\IEnumObjects_Next.htm
tech.root: shell
ms.assetid: 5c79d3e2-c1c9-4529-9a60-457c2d2e6af5
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IEnumObjects interface [Windows Shell],Next method, IEnumObjects.Next, IEnumObjects::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumObjects interface, _shell_IEnumObjects_Next, shell.IEnumObjects_Next, shobjidl_core/IEnumObjects::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IEnumObjects.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumObjects::Next


## -description


Gets the next specified number and type of objects.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of objects to retrieve.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired interface ID.


### -param rgelt [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>.


### -param pceltFetched [out, optional]

Type: <b>ULONG*</b>

Pointer to a <b>ULONG</b> value that, when this method returns, states the actual number of objects retrieved. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the method successfully retrieved the requested objects. This method only returns S_OK if the full count of requested items are successfully retrieved.
                    
                    

S_FALSE indicates that more items were requested than remained in the enumeration.



