---
UID: NF:imapi2fs.IBootOptions.put_Manufacturer
title: IBootOptions::put_Manufacturer
author: windows-sdk-content
description: Sets an identifier that identifies the manufacturer or developer of the CD.
old-location: imapi\ibootoptions_put_manufacturer.htm
old-project: imapi
ms.assetid: 485b36f0-6c33-48da-8ac5-64f4fc13fd68
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IBootOptions interface [IMAPI],put_Manufacturer method, IBootOptions.put_Manufacturer, IBootOptions::put_Manufacturer, imapi.ibootoptions_put_manufacturer, imapi2fs/IBootOptions::put_Manufacturer, put_Manufacturer, put_Manufacturer method [IMAPI], put_Manufacturer method [IMAPI],IBootOptions interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IBootOptions.put_Manufacturer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IBootOptions::put_Manufacturer


## -description


Sets an identifier that identifies the manufacturer or developer of the CD.


## -parameters




### -param newVal [in]

Identifier that identifies the manufacturer or developer of the CD. This is an ANSI string that is limited to 24 bytes. The string does not need to include a NULL character; however, you must set unused bytes to 0x00.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>	IMAPI_E_INVALID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The provided <i>newVal</i> parameter is not valid.

Value: 0xC0AAB101

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/446b535c-d576-4f96-8b74-305e34cb99d4">IBootOptions</a>



<a href="https://msdn.microsoft.com/e9c75760-42e8-4ad0-aa5c-82bfdc1327af">IBootOptions::get_Manufacturer</a>
 

 

