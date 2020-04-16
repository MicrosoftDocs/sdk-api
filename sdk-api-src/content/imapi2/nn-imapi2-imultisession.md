---
UID: NN:imapi2.IMultisession
title: IMultisession (imapi2.h)
description: Base interface containing properties common to derived multisession interfaces.helpviewer_keywords: ["IMultisession","IMultisession interface [IMAPI]","IMultisession interface [IMAPI]","described","imapi.imultisession","imapi2/IMultisession"]
old-location: imapi\imultisession.htm
tech.root: imapi
ms.assetid: a983af02-ee0e-4a62-8ae0-fb9a1e0c2571
ms.date: 12/05/2018
ms.keywords: IMultisession, IMultisession interface [IMAPI], IMultisession interface [IMAPI],described, imapi.imultisession, imapi2/IMultisession
f1_keywords:
- imapi2/IMultisession
dev_langs:
- c++
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
- imapi2.h
api_name:
- IMultisession
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMultisession interface


## -description


Base interface containing properties common to derived multisession interfaces.

You can derive from this interface to implement a new multi-session mechanism that is different from <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential">IMultisessionSequential</a> and <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite">IMultisessionRandomWrite</a>. For example, you could implement a mechanism for BD-R Pseudo-Overwrite. 

To access media-specific properties of a multisession interface, use the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential">IMultisessionSequential</a> and <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite">IMultisessionRandomWrite</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultisession</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMultisession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMultisession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-imultisession-get_importrecorder">get_ImportRecorder</a>
</td>
<td align="left" width="63%">
Retrieves the disc recorder to use to import one or more previous sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-imultisession-get_inuse">get_InUse</a>
</td>
<td align="left" width="63%">
Determines if this multi-session type is the one you should use on the current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-imultisession-get_issupportedoncurrentmediastate">get_IsSupportedOnCurrentMediaState</a>
</td>
<td align="left" width="63%">
Determines if the multi-session type can write to the current optical media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-imultisession-put_inuse">put_InUse</a>
</td>
<td align="left" width="63%">
Determines if this multi-session type is the one you should use on the current media.

</td>
</tr>
</table> 


## -remarks



If more than one multi-session interface exist, the application can let <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a> choose a compatible multi-session interface to use  or the application can specify the multi-session interface to use by setting the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-imultisession-put_inuse">put_InUse</a> property to VARIANT_TRUE.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

