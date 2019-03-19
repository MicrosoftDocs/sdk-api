---
UID: NS:winnt._REPARSE_GUID_DATA_BUFFER
title: REPARSE_GUID_DATA_BUFFER (winnt.h)
author: windows-sdk-content
description: Contains information about a reparse point.
old-location: fs\reparse_guid_data_buffer_str.htm
tech.root: FileIO
ms.assetid: 2d49c1bc-0b1d-40b1-a3a2-6b30f0b3cca0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PREPARSE_GUID_DATA_BUFFER, PREPARSE_GUID_DATA_BUFFER, PREPARSE_GUID_DATA_BUFFER structure pointer [Files], REPARSE_GUID_DATA_BUFFER, REPARSE_GUID_DATA_BUFFER structure [Files], _REPARSE_GUID_DATA_BUFFER, _win32_reparse_guid_data_buffer_str, base.reparse_guid_data_buffer_str, fs.reparse_guid_data_buffer_str, winnt/PREPARSE_GUID_DATA_BUFFER, winnt/REPARSE_GUID_DATA_BUFFER"
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - REPARSE_GUID_DATA_BUFFER
product: Windows
targetos: Windows
req.typenames: REPARSE_GUID_DATA_BUFFER, *PREPARSE_GUID_DATA_BUFFER
req.redist: 
---

# REPARSE_GUID_DATA_BUFFER structure


## -description


Contains information about a reparse point. It is used by the 
    <a href="https://msdn.microsoft.com/6f1b7ea2-aed6-4ab4-8e92-1b77ab5cfefb">FSCTL_GET_REPARSE_POINT</a> control code.


## -struct-fields




### -field ReparseTag

The reparse point tag. This member identifies the structure of the user-defined reparse data. For more 
      information, see <a href="https://msdn.microsoft.com/d02a2f50-d374-4149-bc04-49b7db052f62">Reparse Point Tags</a>.


### -field ReparseDataLength

The size of the reparse data in the <b>DataBuffer</b> member, in bytes. This value may 
      vary with different tags and may vary between two uses of the same tag.


### -field Reserved

Reserved; do not use.


### -field ReparseGuid

A <b>GUID</b> that uniquely identifies the  reparse point. When setting a reparse 
      point, the application must provide a non-NULL <b>GUID</b> in the 
      <b>ReparseGuid</b> member. When retrieving a reparse point from the file system, 
      <b>ReparseGuid</b> is the <b>GUID</b> assigned when the reparse point 
      was set. 
     


### -field GenericReparseBuffer


### -field GenericReparseBuffer.DataBuffer

The user-defined data for the reparse point. The contents are determined by the reparse point implementer. 
       The tag in the <b>ReparseTag</b> member and the <b>GUID</b> in the 
       <b>ReparseGuid</b> member indicate how the data is to be interpreted.


## -remarks



The <b>REPARSE_GUID_DATA_BUFFER</b> structure is 
    used by all third-party layered drivers to store data for a reparse point. Each reparse point contains one 
    instance of a <b>REPARSE_GUID_DATA_BUFFER</b> 
    structure.




## -see-also




<a href="https://msdn.microsoft.com/6f1b7ea2-aed6-4ab4-8e92-1b77ab5cfefb">FSCTL_GET_REPARSE_POINT</a>



<a href="https://msdn.microsoft.com/3abb3a08-9a00-43eb-9792-82eab1a25f06">Reparse Points</a>
 

 

