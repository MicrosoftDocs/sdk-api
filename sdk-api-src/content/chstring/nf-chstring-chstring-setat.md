---
UID: NF:chstring.CHString.SetAt
title: CHString::SetAt (chstring.h)
description: Overwrites one character specified by an index number.
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","SetAt method","CHString.SetAt","CHString::SetAt","SetAt","SetAt method [Windows Management Instrumentation]","SetAt method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_setat","chstring/CHString::SetAt","wmi.chstring_setat"]
old-location: wmi\chstring_setat.htm
tech.root: wmi
ms.assetid: ccac0f07-a272-41b0-950c-7e5d97d9f1d7
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],SetAt method, CHString.SetAt, CHString::SetAt, SetAt, SetAt method [Windows Management Instrumentation], SetAt method [Windows Management Instrumentation],CHString interface, _hmm_chstring_setat, chstring/CHString::SetAt, wmi.chstring_setat
req.header: chstring.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CHString::SetAt
 - chstring/CHString::SetAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString.SetAt
---

# CHString::SetAt


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetAt</b> method overwrites one character specified by an index number. If the index exceeds the bounds of the existing string,  <b>SetAt</b> does not enlarge the string.

## -parameters

### -param nIndex

Zero-based index of the character in the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string.

<div class="alert"><b>Note</b>  The <i>nIndex</i> parameter must be greater than or equal to zero (0), and less than the value returned by <a href="/windows/desktop/api/chstring/nf-chstring-chstring-getlength">GetLength</a>. The debug version of the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> library validates the bounds of <i>nIndex</i>; the release version does not.</div>
<div> </div>

### -param ch

The character to insert.

## -returns

This method does not return a value.

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-getat(int)">CHString::GetAt</a>