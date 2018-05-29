---
UID: NF:mfidl.MFShutdownObject
title: MFShutdownObject function
author: windows-sdk-content
description: Shuts down a Media Foundation object and releases all resources associated with the object.
old-location: mf\mfshutdownobject.htm
old-project: medfound
ms.assetid: a7dc3d4a-f21e-4af8-bee0-2d5f2cf28587
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFShutdownObject, MFShutdownObject function [Media Foundation], a7dc3d4a-f21e-4af8-bee0-2d5f2cf28587, mf.mfshutdownobject, mfidl/MFShutdownObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFShutdownObject
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFShutdownObject function


## -description


Shuts down a Media Foundation object and releases all resources associated with the object.

This function is a helper function that wraps the <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">IMFShutdown::Shutdown</a> method. The function queries the object for the <a href="https://msdn.microsoft.com/c3052658-51bb-401b-8db9-3428868899d6">IMFShutdown</a> interface and, if successful, calls <b>Shutdown</b> on the object.


## -parameters




### -param pUnk

Pointer to the <b>IUnknown</b> interface of the object.


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
 




## -remarks



This function is not related to the <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a> function, which shuts down the Media Foundation platform, as described in <a href="https://msdn.microsoft.com/e4db81d3-7a9e-47d7-8611-6dac8026259c">Initializing Media Foundation</a>.






## -see-also




<a href="https://msdn.microsoft.com/c3052658-51bb-401b-8db9-3428868899d6">IMFShutdown</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

