---
UID: NF:oledlg.IOleUIObjInfoA.ConvertObject
title: IOleUIObjInfoA::ConvertObject
author: windows-sdk-content
description: Converts the object to the type of the specified CLSID.
old-location: com\ioleuiobjinfo_convertobject.htm
old-project: com
ms.assetid: 44611ed3-35de-4b20-adae-d3a28aa11944
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ConvertObject, ConvertObject method [COM], ConvertObject method [COM],IOleUIObjInfo interface, ConvertObject method [COM],IOleUIObjInfoA interface, ConvertObject method [COM],IOleUIObjInfoW interface, IOleUIObjInfo interface [COM],ConvertObject method, IOleUIObjInfo::ConvertObject, IOleUIObjInfoA interface [COM],ConvertObject method, IOleUIObjInfoA.ConvertObject, IOleUIObjInfoA::ConvertObject, IOleUIObjInfoW interface [COM],ConvertObject method, IOleUIObjInfoW::ConvertObject, _ole_IOleUIObjInfo_ConvertObject, com.ioleuiobjinfo_convertobject, oledlg/IOleUIObjInfo::ConvertObject, oledlg/IOleUIObjInfoA::ConvertObject, oledlg/IOleUIObjInfoW::ConvertObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OLEUIPASTEFLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleDlg.h
api_name:
-	IOleUIObjInfo.ConvertObject
-	IOleUIObjInfoW.ConvertObject
-	IOleUIObjInfoA.ConvertObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleUIObjInfoA::ConvertObject


## -description


Converts the object to the type of the specified CLSID.


## -parameters




### -param dwObject [in]

A unique identifier for the object.


### -param clsidNew [in]

The CLSID.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Insufficient access permissions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified identifier is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation of <b>IOleUIObjInfo::ConvertObject</b> needs to convert the object to the CLSID specified. The actions taken by the convert operation are similar to the actions taken after calling <a href="https://msdn.microsoft.com/3af4b321-cea2-4f88-ae22-2dcefbb2c2ad">OleUIConvert</a>.




## -see-also




<a href="https://msdn.microsoft.com/508dccb3-e98b-4f62-8bc3-98ca2b0d1349">IOleUIObjInfo</a>



<a href="https://msdn.microsoft.com/3af4b321-cea2-4f88-ae22-2dcefbb2c2ad">OleUIConvert</a>
 

 

