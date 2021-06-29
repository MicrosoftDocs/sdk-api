---
UID: NF:vswriter.CVssWriter.GetCurrentLevel
title: CVssWriter::GetCurrentLevel (vswriter.h)
description: The GetCurrentLevel method returns the current application level.
helpviewer_keywords: ["CVssWriter interface [VSS]","GetCurrentLevel method","CVssWriter.GetCurrentLevel","CVssWriter::GetCurrentLevel","GetCurrentLevel","GetCurrentLevel method [VSS]","GetCurrentLevel method [VSS]","CVssWriter interface","_win32_cvsswriter_getcurrentlevel","base.cvsswriter_getcurrentlevel","vswriter/CVssWriter::GetCurrentLevel"]
old-location: base\cvsswriter_getcurrentlevel.htm
tech.root: base
ms.assetid: 09540f57-832a-49ca-9b64-e7660b331192
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],GetCurrentLevel method, CVssWriter.GetCurrentLevel, CVssWriter::GetCurrentLevel, GetCurrentLevel, GetCurrentLevel method [VSS], GetCurrentLevel method [VSS],CVssWriter interface, _win32_cvsswriter_getcurrentlevel, base.cvsswriter_getcurrentlevel, vswriter/CVssWriter::GetCurrentLevel
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
 - CVssWriter::GetCurrentLevel
 - vswriter/CVssWriter::GetCurrentLevel
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
 - CVssWriter.GetCurrentLevel
---

# CVssWriter::GetCurrentLevel


## -description

The 
<b>GetCurrentLevel</b> method returns the current application level.

<b>GetCurrentLevel</b> is a protected method implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.



## -returns

This method returns a writer's current application level as a 
<a href="/windows/desktop/api/vss/ne-vss-vss_application_level">VSS_APPLICATION_LEVEL</a> enumeration value. See 
<b>VSS_APPLICATION_LEVEL</b> for a description of these values.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_application_level">VSS_APPLICATION_LEVEL</a>
