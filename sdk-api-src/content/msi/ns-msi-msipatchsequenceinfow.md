---
UID: NS:msi.tagMSIPATCHSEQUENCEINFOW
title: MSIPATCHSEQUENCEINFOW (msi.h)
description: The MSIPATCHSEQUENCEINFO structure is used by the MsiDeterminePatchSequence and MsiDetermineApplicablePatches functions. (Unicode)
helpviewer_keywords: ["*PMSIPATCHSEQUENCEINFOW","MSIPATCHSEQUENCEINFO","MSIPATCHSEQUENCEINFO structure","MSIPATCHSEQUENCEINFOA","MSIPATCHSEQUENCEINFOW","MSIPATCH_DATATYPE_PATCHFILE","MSIPATCH_DATATYPE_XMLBLOB","MSIPATCH_DATATYPE_XMLPATH","PMSIPATCHSEQUENCEINFO","PMSIPATCHSEQUENCEINFO structure pointer","msi/MSIPATCHSEQUENCEINFO","msi/MSIPATCHSEQUENCEINFOA","msi/MSIPATCHSEQUENCEINFOW","msi/PMSIPATCHSEQUENCEINFO","setup.msipatchsequenceinfo"]
old-location: setup\msipatchsequenceinfo.htm
tech.root: setup
ms.assetid: 75f76d85-39f6-4a2c-8b5f-1238639a2014
ms.date: 12/05/2018
ms.keywords: '*PMSIPATCHSEQUENCEINFOW, MSIPATCHSEQUENCEINFO, MSIPATCHSEQUENCEINFO structure, MSIPATCHSEQUENCEINFOA, MSIPATCHSEQUENCEINFOW, MSIPATCH_DATATYPE_PATCHFILE, MSIPATCH_DATATYPE_XMLBLOB, MSIPATCH_DATATYPE_XMLPATH, PMSIPATCHSEQUENCEINFO, PMSIPATCHSEQUENCEINFO structure pointer, msi/MSIPATCHSEQUENCEINFO, msi/MSIPATCHSEQUENCEINFOA, msi/MSIPATCHSEQUENCEINFOW, msi/PMSIPATCHSEQUENCEINFO, setup.msipatchsequenceinfo'
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MSIPATCHSEQUENCEINFOW (Unicode) and MSIPATCHSEQUENCEINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MSIPATCHSEQUENCEINFOW, *PMSIPATCHSEQUENCEINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMSIPATCHSEQUENCEINFOW
 - msi/tagMSIPATCHSEQUENCEINFOW
 - PMSIPATCHSEQUENCEINFOW
 - msi/PMSIPATCHSEQUENCEINFOW
 - MSIPATCHSEQUENCEINFOW
 - msi/MSIPATCHSEQUENCEINFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msi.h
api_name:
 - MSIPATCHSEQUENCEINFO
 - MSIPATCHSEQUENCEINFOA
 - MSIPATCHSEQUENCEINFOW
---

# MSIPATCHSEQUENCEINFOW structure


## -description

The <b>MSIPATCHSEQUENCEINFO</b> structure  is used by the <a href="/windows/desktop/api/msi/nf-msi-msideterminepatchsequencea">MsiDeterminePatchSequence</a> and <a href="/windows/desktop/api/msi/nf-msi-msidetermineapplicablepatchesa">MsiDetermineApplicablePatches</a> functions.

## -struct-fields

### -field szPatchData

Pointer to the path of a patch file, an XML blob, or an XML file.

### -field ePatchDataType

Qualifies <b>szPatchData</b> as a patch file, an XML blob, or an XML file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIPATCH_DATATYPE_PATCHFILE"></a><a id="msipatch_datatype_patchfile"></a><dl>
<dt><b>MSIPATCH_DATATYPE_PATCHFILE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The <b>szPatchData</b> member refers to a path of a patch file.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIPATCH_DATATYPE_XMLPATH"></a><a id="msipatch_datatype_xmlpath"></a><dl>
<dt><b>MSIPATCH_DATATYPE_XMLPATH</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The <b>szPatchData</b> member refers to a path of a XML file.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIPATCH_DATATYPE_XMLBLOB"></a><a id="msipatch_datatype_xmlblob"></a><dl>
<dt><b>MSIPATCH_DATATYPE_XMLBLOB</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The <b>szPatchData</b> member refers to an XML blob.

</td>
</tr>
</table>

### -field dwOrder

Set to an integer that indicates the sequence of the patch in the order of application. The sequence starts with 0. If a patch is not applicable to the specified .msi file, or if the function fails, <b>dwOrder</b> is set to -1.

### -field uStatus

Set to ERROR_SUCCESS or the corresponding Win32 error code.

## -see-also

<a href="/windows/desktop/api/msi/nf-msi-msidetermineapplicablepatchesa">MsiDetermineApplicablePatches</a>



<a href="/windows/desktop/api/msi/nf-msi-msideterminepatchsequencea">MsiDeterminePatchSequence</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>

## -remarks

> [!NOTE]
> The msi.h header defines MSIPATCHSEQUENCEINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
