---
UID: NN:mfidl.IMFFieldOfUseMFTUnlock
title: IMFFieldOfUseMFTUnlock (mfidl.h)
description: Enables an application to use a Media Foundation transform (MFT) that has restrictions on its use.
helpviewer_keywords: ["IMFFieldOfUseMFTUnlock","IMFFieldOfUseMFTUnlock interface [Media Foundation]","IMFFieldOfUseMFTUnlock interface [Media Foundation]","described","mf.imffieldofusemftunlock","mfidl/IMFFieldOfUseMFTUnlock"]
old-location: mf\imffieldofusemftunlock.htm
tech.root: medfound
ms.assetid: b144589b-d559-4686-b617-0e3c393380e9
ms.date: 12/05/2018
ms.keywords: IMFFieldOfUseMFTUnlock, IMFFieldOfUseMFTUnlock interface [Media Foundation], IMFFieldOfUseMFTUnlock interface [Media Foundation],described, mf.imffieldofusemftunlock, mfidl/IMFFieldOfUseMFTUnlock
f1_keywords:
- mfidl/IMFFieldOfUseMFTUnlock
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfidl.h
api_name:
- IMFFieldOfUseMFTUnlock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFFieldOfUseMFTUnlock interface


## -description


Enables an application to use a Media Foundation transform (MFT) that has restrictions on its use.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFFieldOfUseMFTUnlock</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFFieldOfUseMFTUnlock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFFieldOfUseMFTUnlock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock">Unlock</a>
</td>
<td align="left" width="63%">
Unlocks an MFT so that the application can use it.

</td>
</tr>
</table> 


## -remarks



If you register an MFT that requires unlocking, include the <b>MFT_ENUM_FLAG_FIELDOFUSE</b> flag when you call the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/field-of-use-restrictions">Field of Use Restrictions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/mft-fieldofuse-unlock-attribute">MFT_FIELDOFUSE_UNLOCK_Attribute</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

