---
UID: NF:wdsclientapi.WdsCliGetEnumerationFlags
title: WdsCliGetEnumerationFlags function (wdsclientapi.h)
description: Returns the image enumeration flag for the current image handle.
helpviewer_keywords: ["WdsCliFlagEnumFilterVersion","WdsCliGetEnumerationFlags","WdsCliGetEnumerationFlags function [Windows Deployment Services]","wds.wdscligetenumerationflags","wdsclientapi/WdsCliGetEnumerationFlags"]
old-location: wds\wdscligetenumerationflags.htm
tech.root: wds
ms.assetid: 689ef310-c7e6-4ba0-9784-8cc8a8a43724
ms.date: 12/05/2018
ms.keywords: WdsCliFlagEnumFilterVersion, WdsCliGetEnumerationFlags, WdsCliGetEnumerationFlags function [Windows Deployment Services], wds.wdscligetenumerationflags, wdsclientapi/WdsCliGetEnumerationFlags
req.header: wdsclientapi.h
req.include-header: WdsClientAPI.h
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
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsCliGetEnumerationFlags
 - wdsclientapi/WdsCliGetEnumerationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliGetEnumerationFlags
---

# WdsCliGetEnumerationFlags function


## -description

Returns the image enumeration flag for the current image handle.

## -parameters

### -param Handle [in]

A find handle returned by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function.

### -param pdwFlags [out]

A pointer to a value that receives the enumeration flag value.


This parameter can have the following values



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WdsCliFlagEnumFilterVersion"></a><a id="wdscliflagenumfilterversion"></a><a id="WDSCLIFLAGENUMFILTERVERSION"></a><dl>
<dt><b>WdsCliFlagEnumFilterVersion</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The WDS client only shows images that have the same version as the boot image. 

</td>
</tr>
</table>

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a>



<a href="/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>