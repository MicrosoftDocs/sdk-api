---
UID: NF:gdiplusheaders.Metafile.PlayRecord
title: Metafile::PlayRecord
author: windows-sdk-content
description: The Metafile::PlayRecord method plays a metafile record.
old-location: gdiplus\_gdiplus_CLASS_Metafile_PlayRecord_recordType_flags_dataSize_data_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafilemethods\playrecord.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Metafile class [GDI+],PlayRecord method, Metafile.PlayRecord, Metafile::PlayRecord, PlayRecord, PlayRecord method [GDI+], PlayRecord method [GDI+],Metafile class, _gdiplus_CLASS_Metafile_PlayRecord_recordType_flags_dataSize_data_, gdiplus._gdiplus_CLASS_Metafile_PlayRecord_recordType_flags_dataSize_data_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Metafile.PlayRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Metafile::PlayRecord


## -description


The <b>Metafile::PlayRecord</b> method plays a metafile record.


## -parameters




### -param recordType [in]

Type: <b><a href="https://msdn.microsoft.com/520852c1-961e-4deb-9e3a-49ad753fa861">EmfPlusRecordType</a></b>

Element of the <a href="https://msdn.microsoft.com/520852c1-961e-4deb-9e3a-49ad753fa861">EmfPlusRecordType</a> enumeration that specifies the type of metafile record to be played. 


### -param flags [in]

Type: <b>UINT</b>

Set of flags that specify attributes of the record to be played. 


### -param dataSize [in]

Type: <b>UINT</b>

Integer that specifies the number of bytes contained in the record data. 


### -param data [in]

Type: <b>const BYTE*</b>

Pointer to an array of bytes that contains the record data. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 

						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 

						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



This method is used in conjunction with the <a href="https://msdn.microsoft.com/167a04d5-24f4-4885-b97c-b4536e41e125">EnumerateMetafile Methods</a> method of the 

				<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> class. The EnumerateMetafile Methods method calls an application-defined callback function for each record in a specified metafile. The callback function can display each record (or selected records) by calling the <b>Metafile::PlayRecord</b> method.




## -see-also




<a href="https://msdn.microsoft.com/520852c1-961e-4deb-9e3a-49ad753fa861">EmfPlusRecordType</a>



<a href="https://msdn.microsoft.com/167a04d5-24f4-4885-b97c-b4536e41e125">EnumerateMetafile Methods</a>



<a href="https://msdn.microsoft.com/79b8df1b-6fc5-455b-9d08-57d64bf6bffa">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077">Metafiles</a>
 

 

