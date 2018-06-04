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

# ITextDocument2::RangeFromPoint2


## -description


Retrieves the degenerate range at (or nearest to) a particular point on the screen.


## -parameters




### -param x [in]

Type: <b>long</b>

The x-coordinate of a point, in screen coordinates.


### -param y [in]

Type: <b>long</b>

The y-coordinate of a point, in screen coordinates.


### -param Type [in]

Type: <b>long</b>

The alignment type of the specified point. For a list of valid values, see <a href="https://msdn.microsoft.com/67bb38d8-d96d-4d17-876d-4cadc39adece">ITextRange::GetPoint</a>.


### -param ppRange [out, retval]

Type: <b>ITextRange2**</b>


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

