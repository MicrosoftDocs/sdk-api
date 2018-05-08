---
UID: NF:mfapi.MFCreateMediaEvent
title: MFCreateMediaEvent function
author: windows-driver-content
description: Creates a media event object.
old-location: mf\mfcreatemediaevent.htm
old-project: medfound
ms.assetid: 64da695e-5f56-4f23-9a06-0b0c358e3cc3
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 64da695e-5f56-4f23-9a06-0b0c358e3cc3, MFCreateMediaEvent, MFCreateMediaEvent function [Media Foundation], mf.mfcreatemediaevent, mfapi/MFCreateMediaEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFCreateMediaEvent
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateMediaEvent function


## -description



Creates a media event object.




## -parameters




### -param met

The event type. See <a href="https://msdn.microsoft.com/b62e0d9f-dada-4b75-a8d3-568ee2955888">IMFMediaEvent::GetType</a>. For a list of event types, see <a href="https://msdn.microsoft.com/d925f63d-3359-4ba1-802f-0c2b11a3f973">Media Foundation Events</a>.


### -param guidExtendedType

The extended type. See <a href="https://msdn.microsoft.com/56284491-6f84-467e-9fac-46b04db4024a">IMFMediaEvent::GetExtendedType</a>. If the event type does not have an extended type, use the value GUID_NULL.


### -param hrStatus

The event status. See <a href="https://msdn.microsoft.com/e2fc6c81-11c0-4947-b647-3e74a73ee5a2">IMFMediaEvent::GetStatus</a>



### -param pvValue

The value associated with the event, if any. See <a href="https://msdn.microsoft.com/05e57b40-2565-4312-866e-50f0c7d62c4a">IMFMediaEvent::GetValue</a>. This parameter can be <b>NULL</b>.


### -param ppEvent

Receives a pointer to the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface. The caller must release the interface.


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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

