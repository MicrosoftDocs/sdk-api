---
UID: NF:wmcontainer.MFCreateASFProfile
title: MFCreateASFProfile function (wmcontainer.h)
author: windows-sdk-content
description: Creates the ASF profile object.
old-location: mf\mfcreateasfprofile.htm
tech.root: medfound
ms.assetid: fa57fac7-a191-4d5b-89be-319af7b3e09c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFCreateASFProfile, MFCreateASFProfile function [Media Foundation], fa57fac7-a191-4d5b-89be-319af7b3e09c, mf.mfcreateasfprofile, wmcontainer/MFCreateASFProfile
ms.topic: function
req.header: wmcontainer.h
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateASFProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateASFProfile function


## -description



Creates the ASF profile object.




## -parameters




### -param ppIProfile

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a> interface. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

