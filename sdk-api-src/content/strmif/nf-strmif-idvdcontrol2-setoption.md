---
UID: NF:strmif.IDvdControl2.SetOption
title: IDvdControl2::SetOption
author: windows-sdk-content
description: The SetOption method enables or disables an internal behavior flag on the DVD Navigator filter.
old-location: dshow\idvdcontrol2_setoption.htm
tech.root: DirectShow
ms.assetid: b3b28da8-b0cb-4d76-8184-93572e4b6d06
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IDvdControl2 interface [DirectShow],SetOption method, IDvdControl2.SetOption, IDvdControl2::SetOption, IDvdControl2SetOption, SetOption, SetOption method [DirectShow], SetOption method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_setoption, strmif/IDvdControl2::SetOption
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.SetOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl2::SetOption


## -description



The <b>SetOption</b> method enables or disables an internal behavior flag on the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter.




## -parameters




### -param flag [in]

Specifies which behavior to modify, as a member of the <a href="https://msdn.microsoft.com/29e75f58-58f3-4b3f-a3ba-e3451d3a0cae">DVD_OPTION_FLAG</a> enumeration type. 


### -param fState

TBD




#### - bEnable [in]

Specifies the new value of the option given in the <i>flag</i> parameter.

<div class="alert"><b>Note</b>  This parameter is a <b>BOOL</b> type, but some options treat this parameter as a numeric value, not a Boolean value. For details, see the <a href="https://msdn.microsoft.com/29e75f58-58f3-4b3f-a3ba-e3451d3a0cae">DVD_OPTION_FLAG</a> reference page.
          </div>
<div> </div>

## -returns



Returns one of the following values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid flag.

</td>
</tr>
</table>
 




## -remarks



Call <b>SetOption</b> with the desired flags immediately after creating an instance of the DVD Navigator and whenever you want to change any behaviors.
      

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.
      

<table>
<tr>
<th>Annex J Command Name
            </th>
<th>Valid Domains
            </th>
</tr>
<tr>
<td>None</td>
<td>All</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>
 

 

