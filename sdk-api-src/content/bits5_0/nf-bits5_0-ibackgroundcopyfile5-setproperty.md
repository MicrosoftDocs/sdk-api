---
UID: NF:bits5_0.IBackgroundCopyFile5.SetProperty
title: IBackgroundCopyFile5::SetProperty
author: windows-sdk-content
description: Sets a generic property of a BITS file transfer.
old-location: bits\ibackgroundcopyfile5_setproperty.htm
old-project: bits
ms.assetid: 7a5809ef-e84f-4566-a5fa-fd63b1dfd15c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IBackgroundCopyFile5 interface [BITS],SetProperty method, IBackgroundCopyFile5.SetProperty, IBackgroundCopyFile5::SetProperty, SetProperty, SetProperty method [BITS], SetProperty method [BITS],IBackgroundCopyFile5 interface, bits.ibackgroundcopyfile5_setproperty, bits5_0/IBackgroundCopyFile5::SetProperty
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITS_FILE_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyFile5.SetProperty
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBackgroundCopyFile5::SetProperty


## -description


Sets a generic property of a BITS file transfer.


## -parameters




### -param PropertyId [in]

Specifies the property to be set.


### -param PropertyValue






#### - ProertyValue [out]

A pointer to a union that specifies the value to be set. The union member appropriate for the property ID is used.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/548b507a-4874-4ccf-829e-13e1ca6cc958">IBackgroundCopyFile5</a>



<a href="https://msdn.microsoft.com/7afe4d11-f611-40ea-be94-7825f95576de">IBackgroundCopyFile5.GetProperty</a>
 

 

