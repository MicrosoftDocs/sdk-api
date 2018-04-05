---
UID: NF:bits5_0.IBackgroundCopyJob5.SetProperty
title: IBackgroundCopyJob5::SetProperty method
author: windows-driver-content
description: A generic method for setting BITS job properties.
old-location: bits\ibackgroundcopyjob5_setproperty.htm
old-project: Bits
ms.assetid: D5DB8A96-7417-4142-BA27-783314835CED
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IBackgroundCopyJob5, IBackgroundCopyJob5 interface [BITS], SetProperty method, IBackgroundCopyJob5::SetProperty, SetProperty method [BITS], SetProperty method [BITS], IBackgroundCopyJob5 interface, SetProperty,IBackgroundCopyJob5.SetProperty, bits.ibackgroundcopyjob5_setproperty, bits5_0/IBackgroundCopyJob5::SetProperty
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
req.typenames: BITS_FILE_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bits.lib
-	Bits.dll
api_name:
-	IBackgroundCopyJob5.SetProperty
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBackgroundCopyJob5::SetProperty method


## -description


A generic method for setting BITS job properties.


## -parameters




### -param PropertyId [in]

The ID of the property that is being set specified as a <a href="https://msdn.microsoft.com/4ED7419E-3435-4F12-B293-1FDC24F40D63">BITS_JOB_PROPERTY_ID</a> enum value.


### -param PropertyValue [in]

The value of the property that is being set. In order to hold a value whose type is appropriate to the property, this value is specified via the <a href="https://msdn.microsoft.com/DF1DDB37-F16F-47FF-B6C1-8C545A827CCB">BITS_JOB_PROPERTY_VALUE</a> union that is composed of all the known property types.


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




<a href="https://msdn.microsoft.com/97481F9D-1F7B-473A-B288-A52E527478A0">IBackgroundCopyJob5</a>



<b>IBackgroundCopyJob5::GetProperty</b>
 

 

