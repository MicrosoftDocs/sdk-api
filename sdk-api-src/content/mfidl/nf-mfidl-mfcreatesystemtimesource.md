---
UID: NF:mfidl.MFCreateSystemTimeSource
title: MFCreateSystemTimeSource function
author: windows-sdk-content
description: Creates a presentation time source that is based on the system time.
old-location: mf\mfcreatesystemtimesource.htm
tech.root: medfound
ms.assetid: f3e7b8d5-fd6c-4d87-86f6-1117ca58bc6f
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: MFCreateSystemTimeSource, MFCreateSystemTimeSource function [Media Foundation], f3e7b8d5-fd6c-4d87-86f6-1117ca58bc6f, mf.mfcreatesystemtimesource, mfidl/MFCreateSystemTimeSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateSystemTimeSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateSystemTimeSource function


## -description



Creates a presentation time source that is based on the system time.




## -parameters




### -param ppSystemTimeSource

Receives a pointer to the object's <a href="https://msdn.microsoft.com/e5fab6b7-0abc-4ad7-89a9-33c673e97ce2">IMFPresentationTimeSource</a> interface. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

