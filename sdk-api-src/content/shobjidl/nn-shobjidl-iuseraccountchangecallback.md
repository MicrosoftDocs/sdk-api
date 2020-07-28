---
UID: NN:shobjidl.IUserAccountChangeCallback
title: IUserAccountChangeCallback (shobjidl.h)
description: Exposes a method which is called when the picture that represents a user account is changed.
helpviewer_keywords: ["IUserAccountChangeCallback","IUserAccountChangeCallback interface [Windows Shell]","IUserAccountChangeCallback interface [Windows Shell]","described","_shell_IUserAccountChangeCallback","shell.IUserAccountChangeCallback","shobjidl/IUserAccountChangeCallback"]
old-location: shell\IUserAccountChangeCallback.htm
tech.root: shell
ms.assetid: de72aa25-7d0c-445c-aa1b-f0f3bdc07d10
ms.date: 12/05/2018
ms.keywords: IUserAccountChangeCallback, IUserAccountChangeCallback interface [Windows Shell], IUserAccountChangeCallback interface [Windows Shell],described, _shell_IUserAccountChangeCallback, shell.IUserAccountChangeCallback, shobjidl/IUserAccountChangeCallback
f1_keywords:
- shobjidl/IUserAccountChangeCallback
dev_langs:
- c++
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
- Shobjidl.h
api_name:
- IUserAccountChangeCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUserAccountChangeCallback interface


## -description


Exposes a method which is called when the picture that represents a user account is changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUserAccountChangeCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUserAccountChangeCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUserAccountChangeCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iuseraccountchangecallback-onpicturechange">OnPictureChange</a>
</td>
<td align="left" width="63%">
Called to send notifications when the picture that represents a user account is changed.

</td>
</tr>
</table> 


## -remarks



Applications that want to notify users through this interface can add their class identifier (CLSID) strings as values under this key: 

                <pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>UserPictureChange</b></pre>


The values under this key are enumerated to create this callback object.



