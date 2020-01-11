---
UID: NF:wmcontainer.IMFASFContentInfo.SetProfile
title: IMFASFContentInfo::SetProfile (wmcontainer.h)
description: Uses profile data from a profile object to configure settings in the ContentInfo object.
old-location: mf\imfasfcontentinfo_setprofile.htm
tech.root: medfound
ms.assetid: 7e7e062d-9507-400a-8cc2-5355c12017f5
ms.date: 12/05/2018
ms.keywords: 7e7e062d-9507-400a-8cc2-5355c12017f5, IMFASFContentInfo interface [Media Foundation],SetProfile method, IMFASFContentInfo.SetProfile, IMFASFContentInfo::SetProfile, SetProfile, SetProfile method [Media Foundation], SetProfile method [Media Foundation],IMFASFContentInfo interface, mf.imfasfcontentinfo_setprofile, wmcontainer/IMFASFContentInfo::SetProfile
f1_keywords:
- wmcontainer/IMFASFContentInfo.SetProfile
dev_langs:
- c++
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFASFContentInfo.SetProfile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFContentInfo::SetProfile


## -description



Uses profile data from a profile object to configure settings in the ContentInfo object.




## -parameters




### -param pIProfile [in]

The <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a> interface of the profile object.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If there is already information in the ContentInfo object when this method is called, it is replaced by the information from the profile object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/asf-contentinfo-object">ASF ContentInfo Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile">IMFASFContentInfo::GetProfile</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/initializing-the-contentinfo-object-of-a-new-asf-file">Initializing the ContentInfo Object of a New ASF File</a>
 

 

