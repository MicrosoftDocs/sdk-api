---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDvdControl2::SetOption


## -description



The <b>SetOption</b> method enables or disables an internal behavior flag on the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter.




## -parameters




### -param flag [in]


            Specifies which behavior to modify, as a member of the <a href="https://msdn.microsoft.com/29e75f58-58f3-4b3f-a3ba-e3451d3a0cae">DVD_OPTION_FLAG</a> enumeration type. 


### -param fState






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
<th>
              Annex J Command Name
            </th>
<th>
              Valid Domains
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
 

 

