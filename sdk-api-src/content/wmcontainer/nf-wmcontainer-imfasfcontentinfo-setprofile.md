---
UID: NF:wmcontainer.IMFASFContentInfo.SetProfile
title: IMFASFContentInfo::SetProfile
author: windows-sdk-content
description: Uses profile data from a profile object to configure settings in the ContentInfo object.
old-location: mf\imfasfcontentinfo_setprofile.htm
tech.root: medfound
ms.assetid: 7e7e062d-9507-400a-8cc2-5355c12017f5
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 7e7e062d-9507-400a-8cc2-5355c12017f5, IMFASFContentInfo interface [Media Foundation],SetProfile method, IMFASFContentInfo.SetProfile, IMFASFContentInfo::SetProfile, SetProfile, SetProfile method [Media Foundation], SetProfile method [Media Foundation],IMFASFContentInfo interface, mf.imfasfcontentinfo_setprofile, wmcontainer/IMFASFContentInfo::SetProfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFContentInfo::SetProfile


## -description



Uses profile data from a profile object to configure settings in the ContentInfo object.




## -parameters




### -param pIProfile [in]

The <a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a> interface of the profile object.


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




<a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ASF ContentInfo Object</a>



<a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a>



<a href="https://msdn.microsoft.com/6f74c896-a0c0-407b-b893-de15863bc2eb">IMFASFContentInfo::GetProfile</a>



<a href="https://msdn.microsoft.com/a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a">Initializing the ContentInfo Object of a New ASF File</a>
 

 

