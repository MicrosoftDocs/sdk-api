---
UID: NF:msctf.ITfRange.ShiftStartRegion
title: ITfRange::ShiftStartRegion
author: windows-sdk-content
description: ITfRange::ShiftStartRegion method
old-location: tsf\itfrange_shiftstartregion.htm
old-project: TSF
ms.assetid: 6e16112a-0cfe-41be-9d9c-4cbcde898c3f
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfRange interface [Text Services Framework],ShiftStartRegion method, ITfRange.ShiftStartRegion, ITfRange::ShiftStartRegion, ShiftStartRegion, ShiftStartRegion method [Text Services Framework], ShiftStartRegion method [Text Services Framework],ITfRange interface, _tsf_itfrange_shiftstartregion_ref, msctf/ITfRange::ShiftStartRegion, tsf.itfrange_shiftstartregion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.ShiftStartRegion
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRange::ShiftStartRegion


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit context obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param dir [in]

Contains one of the <a href="https://msdn.microsoft.com/f6a9f9a2-9691-49c7-a481-47ad2cd67a4d">TfShiftDir</a> values that specifies which adjacent region the start anchor is moved to.


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




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/cda2282f-3d3c-4763-9892-b889b29963a6">
        ITfRange::ShiftEndRegion
      </a>



<a href="https://msdn.microsoft.com/f9f983b1-a5fa-4857-b73c-b879c566d6f6">
        ITfRange::ShiftStart
      </a>



<a href="https://msdn.microsoft.com/f6a9f9a2-9691-49c7-a481-47ad2cd67a4d">
        TfShiftDir
      </a>
 

 

