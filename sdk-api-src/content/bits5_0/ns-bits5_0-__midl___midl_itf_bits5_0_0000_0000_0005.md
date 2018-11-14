---
UID: NS:bits5_0.__MIDL___MIDL_itf_bits5_0_0000_0000_0005
title: "__MIDL___MIDL_itf_bits5_0_0000_0000_0005"
author: windows-sdk-content
description: Provides the property value of a BITS file.
old-location: bits\bits_file_property_value.htm
tech.root: Bits
ms.assetid: 0296014d-d5cc-40f0-a3d3-93d8ea704ce5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BITS_FILE_PROPERTY_VALUE, BITS_FILE_PROPERTY_VALUE union [BITS], __MIDL___MIDL_itf_bits5_0_0000_0000_0005, bits.bits_file_property_value, bits5_0/BITS_FILE_PROPERTY_VALUE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bits5_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits5_0.idl
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
 - Bits5_0.h
api_name:
 - BITS_FILE_PROPERTY_VALUE
product: Windows
targetos: Windows
req.typenames: BITS_FILE_PROPERTY_VALUE
req.redist: 
---

# __MIDL___MIDL_itf_bits5_0_0000_0000_0005 structure


## -description


The <b>BITS_FILE_PROPERTY_VALUE</b> union provides the 
    property value of the BITS file based on a value from the 
    <a href="https://msdn.microsoft.com/A14E301E-029E-43C8-B012-8FFFA652EA40">BITS_FILE_PROPERTY_ID</a> enumeration.


## -struct-fields




### -field String

This value is used when using the property ID 
      enum value <b>BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS</b>. 


## -see-also




<a href="https://msdn.microsoft.com/A14E301E-029E-43C8-B012-8FFFA652EA40">BITS_FILE_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/7afe4d11-f611-40ea-be94-7825f95576de">IBackgroundCopyFile5.GetProperty</a>



<a href="https://msdn.microsoft.com/7a5809ef-e84f-4566-a5fa-fd63b1dfd15c">IBackgroundCopyFile5.SetProperty</a>
 

 

