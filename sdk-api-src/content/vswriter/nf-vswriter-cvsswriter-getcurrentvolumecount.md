---
UID: NF:vswriter.CVssWriter.GetCurrentVolumeCount
title: CVssWriter::GetCurrentVolumeCount (vswriter.h)
description: The GetCurrentVolumeCount method returns the number of volumes in the shadow copy set.
helpviewer_keywords: ["CVssWriter interface [VSS]","GetCurrentVolumeCount method","CVssWriter.GetCurrentVolumeCount","CVssWriter::GetCurrentVolumeCount","GetCurrentVolumeCount","GetCurrentVolumeCount method [VSS]","GetCurrentVolumeCount method [VSS]","CVssWriter interface","_win32_cvsswriter_getcurrentvolumecount","base.cvsswriter_getcurrentvolumecount","vswriter/CVssWriter::GetCurrentVolumeCount"]
old-location: base\cvsswriter_getcurrentvolumecount.htm
tech.root: base
ms.assetid: 5f553a46-10ee-475e-b028-2652c74fbe5d
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],GetCurrentVolumeCount method, CVssWriter.GetCurrentVolumeCount, CVssWriter::GetCurrentVolumeCount, GetCurrentVolumeCount, GetCurrentVolumeCount method [VSS], GetCurrentVolumeCount method [VSS],CVssWriter interface, _win32_cvsswriter_getcurrentvolumecount, base.cvsswriter_getcurrentvolumecount, vswriter/CVssWriter::GetCurrentVolumeCount
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CVssWriter::GetCurrentVolumeCount
 - vswriter/CVssWriter::GetCurrentVolumeCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriter.GetCurrentVolumeCount
---

# CVssWriter::GetCurrentVolumeCount


## -description

The 
<b>GetCurrentVolumeCount</b> method returns the number of volumes in the shadow copy set.

<b>GetCurrentVolumeCount</b> is a protected method implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.



## -returns

This method returns the number of volumes returned in the shadow copy set. This value will also be the size of the array of null-terminated wide character strings containing volume names returned by 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getcurrentvolumearray">CVssWriter::GetCurrentVolumeArray</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getcurrentvolumearray">CVssWriter::GetCurrentVolumeArray</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>
