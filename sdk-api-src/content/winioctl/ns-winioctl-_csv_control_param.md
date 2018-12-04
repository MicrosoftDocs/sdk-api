---
UID: NS:winioctl._CSV_CONTROL_PARAM
title: "_CSV_CONTROL_PARAM"
author: windows-sdk-content
description: Represents a type of CSV control operation.
old-location: fs\csv_control_param.htm
tech.root: fileio
ms.assetid: B984F8CA-3548-4442-8D3B-B2F469F699E1
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PCSV_CONTROL_PARAM, CSV_CONTROL_PARAM, CSV_CONTROL_PARAM structure [Files], PCSV_CONTROL_PARAM, PCSV_CONTROL_PARAM structure pointer [Files], _CSV_CONTROL_PARAM, fs.csv_control_param, winioctl/CSV_CONTROL_PARAM, winioctl/PCSV_CONTROL_PARAM"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - WinIoCtl.h
api_name:
 - CSV_CONTROL_PARAM
product: Windows
targetos: Windows
req.typenames: CSV_CONTROL_PARAM, *PCSV_CONTROL_PARAM
req.redist: 
---

# _CSV_CONTROL_PARAM structure


## -description


Represents a type of CSV control operation.


## -struct-fields




### -field Operation

The type of CSV control operation to undertake.


### -field Unused

Unused.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/6CCCD5CA-FF29-41D4-B687-E403CADABF84">FSCTL_CSV_CONTROL</a> 
    control code to indicate what kind of CSV control operation is being undertaken. It is an alternative to calling 
    that control code by just passing a <a href="https://msdn.microsoft.com/77A2106F-2C07-4A30-BA46-651F74032609">CSV_CONTROL_OP</a> 
    enumeration value, as the structure encapsulates an enumeration value of that type.




## -see-also




<a href="https://msdn.microsoft.com/77A2106F-2C07-4A30-BA46-651F74032609">CSV_CONTROL_OP</a>



<a href="https://msdn.microsoft.com/6CCCD5CA-FF29-41D4-B687-E403CADABF84">FSCTL_CSV_CONTROL</a>



<a href="https://msdn.microsoft.com/406d5c0f-b49a-4075-ac3e-c5b55a0c3fe9">File Management Structures</a>
 

 

