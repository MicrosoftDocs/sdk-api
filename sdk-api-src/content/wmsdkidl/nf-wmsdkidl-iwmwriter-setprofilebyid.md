---
UID: NF:wmsdkidl.IWMWriter.SetProfileByID
title: IWMWriter::SetProfileByID (wmsdkidl.h)
author: windows-sdk-content
description: The SetProfileByID method specifies the profile to use for the current writing task, identifying the profile by its GUID.
old-location: wmformat\iwmwriter_setprofilebyid.htm
tech.root: wmformat
ms.assetid: 743212fd-a1e7-47c5-a220-c203cc2788e6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMWriter interface [windows Media Format],SetProfileByID method, IWMWriter.SetProfileByID, IWMWriter::SetProfileByID, IWMWriterSetProfileByID, SetProfileByID, SetProfileByID method [windows Media Format], SetProfileByID method [windows Media Format],IWMWriter interface, wmformat.iwmwriter_setprofilebyid, wmsdkidl/IWMWriter::SetProfileByID
ms.topic: method
f1_keywords: 
 - "wmsdkidl/IWMWriter.SetProfileByID"
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMWriter.SetProfileByID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriter::SetProfileByID


## -description



The <b>SetProfileByID</b> method specifies the profile to use for the current writing task, identifying the profile by its GUID.




## -parameters




### -param guidProfile [in]

GUID of the profile.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



Only system profiles have IDs. Use the methods of the <b>IWMProfileManager</b> interface to examine system profiles. The header file Wmsysprf.h has a list of system profiles and their IDs.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile">IWMWriter::SetProfile</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/to-use-profiles-with-the-writer">To Use Profiles with the Writer</a>
 

 

