---
UID: NF:bits1_5.IBackgroundCopyJob2.RemoveCredentials
title: IBackgroundCopyJob2::RemoveCredentials (bits1_5.h)
author: windows-sdk-content
description: Removes credentials from use. The credentials must match an existing target and scheme pair that you specified using the IBackgroundCopyJob2::SetCredentials method. There is no method to retrieve the credentials you have set.
old-location: bits\ibackgroundcopyjob2_removecredentials.htm
tech.root: Bits
ms.assetid: dbc6a05d-9e1f-4cc9-b28b-0874aafdfd7c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob2 interface [BITS],RemoveCredentials method, IBackgroundCopyJob2.RemoveCredentials, IBackgroundCopyJob2::RemoveCredentials, RemoveCredentials, RemoveCredentials method [BITS], RemoveCredentials method [BITS],IBackgroundCopyJob2 interface, _drz_ibackgroundcopyjob2_removecredentials, bits.ibackgroundcopyjob2_removecredentials, bits1_5/IBackgroundCopyJob2::RemoveCredentials
ms.topic: method
req.header: bits1_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx2.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx2.dll
api_name:
 - IBackgroundCopyJob2.RemoveCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on  Windows XP
ms.custom: 19H1
---

# IBackgroundCopyJob2::RemoveCredentials


## -description


Removes credentials from use. The credentials must match an existing target and scheme pair that you specified using the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials">IBackgroundCopyJob2::SetCredentials</a> method. There is no method to retrieve the credentials you have set.


## -parameters




### -param Target [in]

Identifies whether to use the credentials for proxy or server authentication.


### -param Scheme [in]

Identifies the authentication scheme to use (basic or one of several challenge-response schemes). For details, see the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/ne-bits1_5-__midl_ibackgroundcopyjob2_0002">BG_AUTH_SCHEME</a> enumeration.


## -returns



This method returns the following return values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No credentials have been set using the given <i>Target</i> and <i>Scheme</i> pair.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/ne-bits1_5-__midl_ibackgroundcopyjob2_0002">BG_AUTH_SCHEME</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/ne-bits1_5-__midl_ibackgroundcopyjob2_0001">BG_AUTH_TARGET</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials">IBackgroundCopyJob2::SetCredentials</a>
 

 

