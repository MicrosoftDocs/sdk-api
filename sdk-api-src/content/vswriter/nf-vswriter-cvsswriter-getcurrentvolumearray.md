---
UID: NF:vswriter.CVssWriter.GetCurrentVolumeArray
title: CVssWriter::GetCurrentVolumeArray (vswriter.h)
description: The GetCurrentVolumeArray method returns the names of the original volumes and the UNC paths of the original remote file shares that belong to the shadow copy set as an array of null-terminated wide character strings.Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  Remote file shares are not supported until Windows 8 and Windows Server 2012.
helpviewer_keywords: ["CVssWriter interface [VSS]","GetCurrentVolumeArray method","CVssWriter.GetCurrentVolumeArray","CVssWriter::GetCurrentVolumeArray","GetCurrentVolumeArray","GetCurrentVolumeArray method [VSS]","GetCurrentVolumeArray method [VSS]","CVssWriter interface","_win32_cvsswriter_getcurrentvolumearray","base.cvsswriter_getcurrentvolumearray","vswriter/CVssWriter::GetCurrentVolumeArray"]
old-location: base\cvsswriter_getcurrentvolumearray.htm
tech.root: base
ms.assetid: 75f72b51-e940-4b1d-88a1-7c35de5a3d87
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],GetCurrentVolumeArray method, CVssWriter.GetCurrentVolumeArray, CVssWriter::GetCurrentVolumeArray, GetCurrentVolumeArray, GetCurrentVolumeArray method [VSS], GetCurrentVolumeArray method [VSS],CVssWriter interface, _win32_cvsswriter_getcurrentvolumearray, base.cvsswriter_getcurrentvolumearray, vswriter/CVssWriter::GetCurrentVolumeArray
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
 - CVssWriter::GetCurrentVolumeArray
 - vswriter/CVssWriter::GetCurrentVolumeArray
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
 - CVssWriter.GetCurrentVolumeArray
---

# CVssWriter::GetCurrentVolumeArray


## -description

The 
<b>GetCurrentVolumeArray</b> method returns the names of the original volumes and the UNC paths of the original remote file shares that belong to the shadow copy set as an array of null-terminated wide character strings.<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012.



<b>GetCurrentVolumeArray</b> is a protected method implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.



## -returns

This method returns a pointer to an <i>n</i>-element array (where <i>n</i> is the value returned by 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getcurrentvolumecount">CVssWriter::GetCurrentVolumeCount</a>) of null-terminated wide character strings that contain the names of the original volumes and the UNC paths of the original remote file shares that belong to the shadow copy set.<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012.



The derived class should not free the memory held by the returned array of volume names. The base class manages the life cycle of the array.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>
