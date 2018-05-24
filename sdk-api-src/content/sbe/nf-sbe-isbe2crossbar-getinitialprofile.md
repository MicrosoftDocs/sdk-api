---
UID: NF:sbe.ISBE2Crossbar.GetInitialProfile
title: ISBE2Crossbar::GetInitialProfile
author: windows-driver-content
description: Gets the initial profile that lists the media types that are present in the currently loaded WTV file.
old-location: mstv\isbe2crossbar_getinitialprofile.htm
old-project: mstv
ms.assetid: 6a4bec40-2c6d-49fb-8977-3c3db2b2b4df
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetInitialProfile, GetInitialProfile method [Microsoft TV Technologies], GetInitialProfile method [Microsoft TV Technologies],ISBE2Crossbar interface, ISBE2Crossbar interface [Microsoft TV Technologies],GetInitialProfile method, ISBE2Crossbar.GetInitialProfile, ISBE2Crossbar::GetInitialProfile, mstv.isbe2crossbar_getinitialprofile, sbe/ISBE2Crossbar::GetInitialProfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbe.h
api_name:
-	ISBE2Crossbar.GetInitialProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISBE2Crossbar::GetInitialProfile


## -description



      Gets the initial profile that lists the media types that are present in the currently loaded WTV file. The media types in the profile correspond to the active pins on a <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter at the time the currently loaded  WTV file is created. The profile is fixed per loaded WTV file and does not change while the filter has a WTV file loaded . However, if the crossbar  is not in default profile mode, you can call the <a href="https://msdn.microsoft.com/34067ca5-ead0-44ac-b274-dc9e3f2fb2fd">SetOutputProfile</a> method to set a new profile for the crossbar. To disable default profile mode, call the <a href="https://msdn.microsoft.com/5038050b-319d-488a-9cea-a2fc59b90cc8">EnableDefaultMode</a> method without the DEF_MODE_PROFILE flag. 


## -parameters




### -param ppProfile [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/b2fb3d08-cbef-4dbf-a60b-8363ccee4fbf">ISBE2MediaTypeProfile</a> interface that implements the profile.
          
          The caller is responsible for releasing this interface. You can use this pointer to create a custom profile that you pass to the <a href="https://msdn.microsoft.com/34067ca5-ead0-44ac-b274-dc9e3f2fb2fd">SetOutputProfile</a> method.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
Null pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_FAIL</dt>
</dl>
</td>
<td width="60%">
Empty initial profiles.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/299816e7-2dad-44a5-a44d-9c3efe405d9b">ISBE2Crossbar</a>



<a href="https://msdn.microsoft.com/b2fb3d08-cbef-4dbf-a60b-8363ccee4fbf">ISBE2MediaTypeProfile</a>



<a href="https://msdn.microsoft.com/155a2e61-3b53-4225-b298-ee51e2afca96">ISBE2SpanningEvent </a>



<a href="https://msdn.microsoft.com/1606eab6-84dc-49ba-8fb6-df3b8615bf85">Stream Buffer Sink2 Filter</a>
 

 

