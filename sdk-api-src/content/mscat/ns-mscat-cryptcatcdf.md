---
UID: NS:mscat.CRYPTCATCDF_
title: CRYPTCATCDF (mscat.h)
description: Contains information used to create a signed catalog file (.cat) from a catalog definition file (CDF).
helpviewer_keywords: ["CRYPTCATCDF","CRYPTCATCDF structure [Security]","mscat/CRYPTCATCDF","security.cryptcatcdf"]
old-location: security\cryptcatcdf.htm
tech.root: security
ms.assetid: 15d5710a-d4df-4e45-b161-5d4f7509ba29
ms.date: 12/05/2018
ms.keywords: CRYPTCATCDF, CRYPTCATCDF structure [Security], mscat/CRYPTCATCDF, security.cryptcatcdf
req.header: mscat.h
req.include-header: 
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
targetos: Windows
req.typenames: CRYPTCATCDF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CRYPTCATCDF_
 - mscat/CRYPTCATCDF_
 - CRYPTCATCDF
 - mscat/CRYPTCATCDF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mscat.h
api_name:
 - CRYPTCATCDF
---

# CRYPTCATCDF structure


## -description

<p class="CCE_Message">[The  <b>CRYPTCATCDF</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTCATCDF</b> structure contains information used to create a signed catalog file (.cat) from a  catalog definition file (CDF). This structure is used by the <a href="/windows/desktop/SecCrypto/makecat">MakeCat</a> tool.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure.

### -field hFile

A handle to the catalog definition file (.cdf).

### -field dwCurFilePos

A value that specifies the current position of the parser measured in bytes from the beginning of the catalog definition file.

### -field dwLastMemberOffset

A value that specifies the number of bytes to the position of the last member parsed in the catalog definition file.

### -field fEOF

An integer that indicates whether the parser finished reading the file. <b>TRUE</b> indicates that the last read operation returned zero bytes.

### -field pwszResultDir

A pointer to a null-terminated string that contains the name of a directory where the catalog file (.cat) will be written.

### -field hCATStore

A handle to the catalog file (.cat).

## -remarks

A parser can update <i>dwCurFilePos</i> and <i>dwLastMemberOffset</i> as it reads the CDF. A user-defined callback function can use this information for recoverable parse errors in the CDF.

## -see-also

<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatcdfclose">CryptCATCDFClose</a>



<a href="/windows/desktop/SecCrypto/cryptcatcdfenumattributeswithcdftag">CryptCATCDFEnumAttributesWithCDFTag</a>



<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatcdfenumcatattributes">CryptCATCDFEnumCatAttributes</a>



<a href="/windows/desktop/SecCrypto/cryptcatcdfenummembersbycdftagex">CryptCATCDFEnumMembersByCDFTagEx</a>



<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatcdfopen">CryptCATCDFOpen</a>



<a href="/windows/desktop/SecCrypto/makecat">MakeCat</a>