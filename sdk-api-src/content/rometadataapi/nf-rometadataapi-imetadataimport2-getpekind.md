---
UID: NF:rometadataapi.IMetaDataImport2.GetPEKind
title: IMetaDataImport2::GetPEKind
author: windows-sdk-content
description: Gets a value identifying the nature of the code in the portable executable (PE) file, typically a DLL or EXE file, that is defined in the current metadata scope.
old-location: winrt\imetadataimport2_getpekind.htm
tech.root: WinRT
ms.assetid: ece40ffa-f92f-4f27-b03c-75204e0c6ee1
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetPEKind, GetPEKind method [Windows Runtime], GetPEKind method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],GetPEKind method, IMetaDataImport2.GetPEKind, IMetaDataImport2::GetPEKind, rometadataapi/IMetaDataImport2::GetPEKind, winrt.imetadataimport2_getpekind
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
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
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport2.GetPEKind
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataImport2::GetPEKind


## -description


Gets a value identifying the nature of the code in the portable executable (PE) file, typically a DLL or EXE file, that is defined in the current metadata scope.


## -parameters




### -param pdwPEKind [out]

 A pointer to a value of the <a href="http://msdn.microsoft.com/en-us/library/ms230275.aspx">CorPEKind</a> enumeration that describes the PE file.


### -param pdwMAchine [out]

A pointer to a value that identifies the architecture of the machine. See the next section for possible values.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The value referenced by the <i>pdwMachine</i> parameter can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Machine architecture</th>
</tr>
<tr>
<td>
IMAGE_FILE_MACHINE_I386



0x014C


</td>
<td>x86
</td>
</tr>
<tr>
<td>
IMAGE_FILE_MACHINE_IA64



0x0200


</td>
<td>Intel IPF
</td>
</tr>
<tr>
<td>
IMAGE_FILE_MACHINE_AMD64



0x8664


</td>
<td>x64
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/32c462e0-d4b8-44db-b24b-c86b46be85bf">IMetaDataImport2</a>
 

 

