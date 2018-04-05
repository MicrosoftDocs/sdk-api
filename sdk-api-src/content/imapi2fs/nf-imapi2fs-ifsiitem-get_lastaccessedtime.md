---
UID: NF:imapi2fs.IFsiItem.get_LastAccessedTime
title: IFsiItem::get_LastAccessedTime method
author: windows-driver-content
description: Retrieves the date and time the directory or file item was last accessed in the file system image.
old-location: imapi\ifsiitem_get_lastaccessedtime.htm
old-project: imapi
ms.assetid: e12f4c62-2dc8-4155-9cd7-0dea982d7b5a
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IFsiItem, IFsiItem interface [IMAPI], get_LastAccessedTime method, IFsiItem::get_LastAccessedTime, get_LastAccessedTime method [IMAPI], get_LastAccessedTime method [IMAPI], IFsiItem interface, get_LastAccessedTime,IFsiItem.get_LastAccessedTime, imapi.ifsiitem_get_lastaccessedtime, imapi2fs/IFsiItem::get_LastAccessedTime
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IFsiItem.get_LastAccessedTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFsiItem::get_LastAccessedTime method


## -description


Retrieves the date and time the directory or file item was last accessed in the file system image.


## -parameters




### -param pVal [out]

Date and time that the item directory or file was last accessed in the file system image, according to UTC time.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



UDFS (UDF) uses the <i>LastAccessedTime</i> value for the <i>CreationTime</i>, as IMAPI does not currently support the <i>CreationTime</i> extended attribue.

CDFS (ISO 9660) sets the <i>LastAccessedTime</i> value retrieved by this method to 0, as only the recording time is stored within the File/Directory descriptor.




## -see-also




<a href="https://msdn.microsoft.com/44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0">IFsiItem</a>



<a href="https://msdn.microsoft.com/6192bff5-9535-4845-9c99-d5ceeea0335f">IFsiItem::put_LastAccessedTime</a>
 

 

