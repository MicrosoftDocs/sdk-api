---
UID: NF:wmcontainer.MFCreateASFMediaSinkActivate
title: MFCreateASFMediaSinkActivate function
author: windows-driver-content
description: Creates an activation object that can be used to create the ASF media sink.
old-location: mf\mfcreateasfmediasinkactivate.htm
old-project: medfound
ms.assetid: 513d0a33-1504-4b88-9629-9e3e0dde3617
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 513d0a33-1504-4b88-9629-9e3e0dde3617, MFCreateASFMediaSinkActivate, MFCreateASFMediaSinkActivate function [Media Foundation], mf.mfcreateasfmediasinkactivate, wmcontainer/MFCreateASFMediaSinkActivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wmcontainer.h
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
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateASFMediaSinkActivate
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# MFCreateASFMediaSinkActivate function


## -description



Creates an activation object that can be used to create the ASF media sink.




## -parameters




### -param pwszFileName

Null-terminated wide-character string that contains the output file name.


### -param pContentInfo

A pointer to the <a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a> interface of an initialized <a href="asf_file_structure.htm">ASF Header Object</a> object. Use this interface to configure the ASF media sink.


### -param ppIActivate

Receives a pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/767d5f1c-2b8d-43b6-916b-035129e93204">Activation Objects</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

