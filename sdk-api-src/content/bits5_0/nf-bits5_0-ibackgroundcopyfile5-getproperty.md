---
UID: NF:bits5_0.IBackgroundCopyFile5.GetProperty
title: IBackgroundCopyFile5::GetProperty
author: windows-sdk-content
description: Gets a generic property of a BITS file transfer.
old-location: bits\ibackgroundcopyfile5_getproperty.htm
tech.root: bits
ms.assetid: 7afe4d11-f611-40ea-be94-7825f95576de
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetProperty, GetProperty method [BITS], GetProperty method [BITS],IBackgroundCopyFile5 interface, IBackgroundCopyFile5 interface [BITS],GetProperty method, IBackgroundCopyFile5.GetProperty, IBackgroundCopyFile5::GetProperty, bits.ibackgroundcopyfile5_getproperty, bits5_0/IBackgroundCopyFile5::GetProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits5_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits5_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyFile5.GetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyFile5::GetProperty


## -description


Gets a generic property of a BITS file transfer.


## -parameters




### -param PropertyId [in]

Specifies the file property whose value is to be retrieved.


### -param PropertyValue [out]

The property value, returned as a pointer to a BITS_FILE_PROPERTY_VALUE union. Use the union field appropriate for the property ID value passed in.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/548b507a-4874-4ccf-829e-13e1ca6cc958">IBackgroundCopyFile5</a>



<a href="https://msdn.microsoft.com/7a5809ef-e84f-4566-a5fa-fd63b1dfd15c">IBackgroundCopyFile5.SetProperty</a>
 

 

