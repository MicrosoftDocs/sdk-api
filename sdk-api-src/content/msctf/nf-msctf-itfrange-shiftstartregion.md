---
UID: NF:msctf.ITfRange.ShiftStartRegion
title: ITfRange::ShiftStartRegion (msctf.h)
author: windows-sdk-content
description: ITfRange::ShiftStartRegion method
old-location: tsf\itfrange_shiftstartregion.htm
tech.root: TSF
ms.assetid: 6e16112a-0cfe-41be-9d9c-4cbcde898c3f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfRange interface [Text Services Framework],ShiftStartRegion method, ITfRange.ShiftStartRegion, ITfRange::ShiftStartRegion, ShiftStartRegion, ShiftStartRegion method [Text Services Framework], ShiftStartRegion method [Text Services Framework],ITfRange interface, _tsf_itfrange_shiftstartregion_ref, msctf/ITfRange::ShiftStartRegion, tsf.itfrange_shiftstartregion
ms.topic: method
f1_keywords: 
 - "msctf/ITfRange.ShiftStartRegion"
dev_langs:
 - c++
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.ShiftStartRegion
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfRange::ShiftStartRegion


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit context obtained from <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.


### -param dir [in]

Contains one of the <a href="https://docs.microsoft.com/windows/win32/api/msctf/ne-msctf-tfshiftdir">TfShiftDir</a> values that specifies which adjacent region the start anchor is moved to.


### -param pfNoRegion [out]

Pointer to a <b>BOOL</b> that receives a flag that indicates if the anchor is positioned adjacent to another region. Receives a nonzero value if the anchor is not adjacent to another region or zero otherwise.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pfNoRegion</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ec</i> does not have a read-only lock.

</td>
</tr>
</table>
 




## -remarks



The start and end positions of a range are called anchors.

The anchor must be positioned adjacent to the desired region prior to calling this method. If it is not, then <i>pfNoRegion</i> receives a nonzero value and the anchor is not moved. If the anchor is adjacent to the desired region, <i>pfNoRegion</i> receives zero and the anchor is moved to the region.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-shiftendregion">ITfRange::ShiftEndRegion
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstart">ITfRange::ShiftStart
      </a>



<a href="https://docs.microsoft.com/windows/win32/api/msctf/ne-msctf-tfshiftdir">TfShiftDir
      </a>
 

 

