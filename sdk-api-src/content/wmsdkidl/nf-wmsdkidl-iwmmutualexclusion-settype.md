---
UID: NF:wmsdkidl.IWMMutualExclusion.SetType
title: IWMMutualExclusion::SetType method
author: windows-driver-content
description: The SetType method specifies the GUID of the type of mutual exclusion required.
old-location: wmformat\iwmmutualexclusion_settype.htm
old-project: wmformat
ms.assetid: 18796219-bc33-41b7-b2af-a23585c2500a
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWMMutualExclusion, IWMMutualExclusion interface [windows Media Format], SetType method, IWMMutualExclusion::SetType, IWMMutualExclusionSetType, SetType method [windows Media Format], SetType method [windows Media Format], IWMMutualExclusion interface, SetType,IWMMutualExclusion.SetType, wmformat.iwmmutualexclusion_settype, wmsdkidl/IWMMutualExclusion::SetType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMMutualExclusion.SetType
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMMutualExclusion::SetType method


## -description



The <b>SetType</b> method specifies the GUID of the type of mutual exclusion required.




## -parameters




### -param guidType [in]

GUID specifying the type of mutual exclusion. For a list of values, see <a href="https://msdn.microsoft.com/546bb0d1-a11e-4bf7-92fc-cef938d792bb">IWMMutualExclusion::GetType</a>



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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid type.

</td>
</tr>
</table>
 




## -remarks



If you create a multiple bit rate audio file, you may encounter problems streaming the file from Windows Media Services 4.1. To avoid problems, disable auto indexing by calling <a href="https://msdn.microsoft.com/6c8f1c25-d752-42b6-87b7-9d6a6e38642f">IWMWriterFileSink3::SetAutoIndexing</a> before writing the file.




## -see-also




<a href="https://msdn.microsoft.com/040635fb-de00-4c8c-9c39-c28c409311c3">IWMMutualExclusion Interface</a>



<a href="https://msdn.microsoft.com/546bb0d1-a11e-4bf7-92fc-cef938d792bb">IWMMutualExclusion::GetType</a>
 

 

