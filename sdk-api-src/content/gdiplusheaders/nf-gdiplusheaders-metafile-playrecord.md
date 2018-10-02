---
UID: NF:gdiplusheaders.Metafile.PlayRecord
title: Metafile::PlayRecord
author: windows-sdk-content
description: The Metafile::PlayRecord method plays a metafile record.
old-location: gdiplus\_gdiplus_CLASS_Metafile_PlayRecord_recordType_flags_dataSize_data_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafilemethods\playrecord.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534110(v=VS.85).aspx">EmfPlusRecordType</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534110(v=VS.85).aspx">EmfPlusRecordType</a> enumeration that specifies the type of metafile record to be played. 


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



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 

						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 

						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



This method is used in conjunction with the <a href="https://msdn.microsoft.com/en-us/library/ms535761(v=VS.85).aspx">EnumerateMetafile Methods</a> method of the 

				<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> class. The EnumerateMetafile Methods method calls an application-defined callback function for each record in a specified metafile. The callback function can display each record (or selected records) by calling the <b>Metafile::PlayRecord</b> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534110(v=VS.85).aspx">EmfPlusRecordType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535761(v=VS.85).aspx">EnumerateMetafile Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533831(v=VS.85).aspx">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536391(v=VS.85).aspx">Metafiles</a>
 

 

