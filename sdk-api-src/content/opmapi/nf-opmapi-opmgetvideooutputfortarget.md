---
UID: NF:opmapi.OPMGetVideoOutputForTarget
title: OPMGetVideoOutputForTarget function
author: windows-sdk-content
description: Returns a video output object for the VidPN target on the specified adapter.
old-location: mf\opmgetvideooutputfortarget.htm
tech.root: medfound
ms.assetid: 736F6C76-D208-49E8-9D96-F54ECE332FCA
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: OPMGetVideoOutputForTarget, OPMGetVideoOutputForTarget function [Media Foundation], OPM_VOS_COPP_SEMANTICS, OPM_VOS_OPM_SEMANTICS, mf.opmgetvideooutputfortarget, opmapi/OPMGetVideoOutputForTarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: opmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - OPMGetVideoOutputForTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OPMGetVideoOutputForTarget function


## -description


Returns a video output object for the VidPN target on the specified adapter.


## -parameters




### -param pAdapterLuid [in]

The LUID for the adapter where the target is located.


### -param VidPnTarget [in]

Target ID for the target on the specified adapter adapter.


### -param vos [in]

A member of the <a href="https://msdn.microsoft.com/d52fbc40-072b-4b7a-87c2-b928563100bb">OPM_VIDEO_OUTPUT_SEMANTICS</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OPM_VOS_OPM_SEMANTICS"></a><a id="opm_vos_opm_semantics"></a><dl>
<dt><b>OPM_VOS_OPM_SEMANTICS</b></dt>
</dl>
</td>
<td width="60%">
The returned <a href="https://msdn.microsoft.com/8bf43577-3535-4f62-ac81-bb7e3c329403">IOPMVideoOutput</a> pointer will use OPM semantics.

</td>
</tr>
<tr>
<td width="40%"><a id="OPM_VOS_COPP_SEMANTICS"></a><a id="opm_vos_copp_semantics"></a><dl>
<dt><b>OPM_VOS_COPP_SEMANTICS</b></dt>
</dl>
</td>
<td width="60%">
The returned <a href="https://msdn.microsoft.com/8bf43577-3535-4f62-ac81-bb7e3c329403">IOPMVideoOutput</a> pointer will use Certified Output Protection Protocol (COPP) semantics.

</td>
</tr>
</table>
 


### -param ppOPMVideoOutput [out]

Receives a pointer to an <a href="https://msdn.microsoft.com/8bf43577-3535-4f62-ac81-bb7e3c329403">IOPMVideoOutput</a> pointer. The caller must release this  pointer.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/8bf43577-3535-4f62-ac81-bb7e3c329403">IOPMVideoOutput</a> interface has two modes of behavior, depending on the value of the <i>vos</i> parameter. If <i>vos</i> is <b>OPM_VOS_COPP_SEMANTICS</b>, <b>IOPMVideoOutput</b> uses COPP semantics. This mode is intended for backward compatibility with COPP. If <i>vos</i> is <b>OPM_VOS_OPM_SEMANTICS</b>, <b>IOPMVideoOutput</b> uses the newer OPM semantics. Differences in behavior are noted on the reference page for each method. The mode does not change during the lifetime of the object.




## -see-also




<a href="https://msdn.microsoft.com/7ecde6ae-56fd-451b-bebb-224c6801be05">OPM Functions</a>
 

 

