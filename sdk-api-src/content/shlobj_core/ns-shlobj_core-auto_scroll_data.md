---
UID: NS:shlobj_core.AUTO_SCROLL_DATA
title: AUTO_SCROLL_DATA (shlobj_core.h)
description: AUTO_SCROLL_DATA may be altered or unavailable.
helpviewer_keywords: ["AUTO_SCROLL_DATA","AUTO_SCROLL_DATA structure [Windows Shell]","_win32_AUTO_SCROLL_DATA_str","shell.AUTO_SCROLL_DATA_str","shlobj_core/AUTO_SCROLL_DATA"]
old-location: shell\AUTO_SCROLL_DATA_str.htm
tech.root: shell
ms.assetid: 4229dd3b-1fc7-4cc7-bcc9-4e25bdc17c11
ms.date: 12/05/2018
ms.keywords: AUTO_SCROLL_DATA, AUTO_SCROLL_DATA structure [Windows Shell], _win32_AUTO_SCROLL_DATA_str, shell.AUTO_SCROLL_DATA_str, shlobj_core/AUTO_SCROLL_DATA
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.typenames: AUTO_SCROLL_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AUTO_SCROLL_DATA
 - shlobj_core/AUTO_SCROLL_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - AUTO_SCROLL_DATA
---

# AUTO_SCROLL_DATA structure


## -description

<p class="CCE_Message">[<b>AUTO_SCROLL_DATA</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Specifies scrolling parameters and keeps track of the last scroll operation.

## -struct-fields

### -field iNextSample

Type: <b>int</b>

A value that indicates the number of times the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_autoscroll">DAD_AutoScroll</a> function has stored data in the structure. The parameter is reset to <code>0</code> after it equals 2.

### -field dwLastScroll

Type: <b>DWORD</b>

A <b>DWORD</b> that indicates the time of the last scroll. The scroll time is also stored in the <b>dwTimes</b> parameter indexed by the current value of <b>iNextSample</b>.

### -field bFull

Type: <b>BOOL</b>

A value that is used to determine whether the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_autoscroll">DAD_AutoScroll</a> function should succeed. This parameter is set to <b>TRUE</b> when the <b>iNextSample</b> parameter is equal to NUM_POINTS.



#### (FALSE)

Default. Indicates that the window should not scroll.



#### (TRUE)

Indicates that the window should scroll.

### -field pts

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>[NUM_POINTS]</b>

A pointer to the current scroll coordinates. The index of this array is <b>iNextSample</b>.

### -field dwTimes

Type: <b>DWORD[NUM_POINTS]</b>

A <b>DWORD</b> that indicates the current scroll time. The index of this array is <b>iNextSample</b>.

## -remarks

NUM_POINTS is currently set to <code>3</code>.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_autoscroll">DAD_AutoScroll</a>

