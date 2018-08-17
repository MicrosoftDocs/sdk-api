---
UID: NF:bits5_0.IBackgroundCopyJob5.GetProperty
title: IBackgroundCopyJob5::GetProperty
author: windows-sdk-content
description: A generic method for getting BITS job properties.
old-location: bits\ibackgroundcopyjob5_getproperty.htm
old-project: bits
ms.assetid: 567C21C7-C689-4A13-9DCA-D45766CB5150
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetProperty, GetProperty method [BITS], GetProperty method [BITS],IBackgroundCopyJob5 interface, IBackgroundCopyJob5 interface [BITS],GetProperty method, IBackgroundCopyJob5.GetProperty, IBackgroundCopyJob5::GetProperty, bits.ibackgroundcopyjob5_getproperty, bits5_0/IBackgroundCopyJob5::GetProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits5_0.h
req.include-header: Bits.h
req.redist: 
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
 - IBackgroundCopyJob5.GetProperty
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBackgroundCopyJob5::GetProperty


## -description


A generic method for getting BITS job properties.


## -parameters




### -param PropertyId [in]

The ID of the property that is being obtained specified as a <a href="https://msdn.microsoft.com/en-us/library/Hh446783(v=VS.85).aspx">BITS_JOB_PROPERTY_ID</a> enum value.


### -param PropertyValue






#### - pPropertyValue [out]

The property value returned as a BITS_JOB_PROPERTY_VALUE union.


## -returns



The method returns the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh446781(v=VS.85).aspx">IBackgroundCopyJob5</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404135(v=VS.85).aspx">IBackgroundCopyJob5::SetProperty</a>
 

 

