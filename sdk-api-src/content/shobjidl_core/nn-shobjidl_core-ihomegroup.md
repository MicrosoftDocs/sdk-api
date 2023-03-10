---
UID: NN:shobjidl_core.IHomeGroup
title: IHomeGroup (shobjidl_core.h)
description: Exposes methods that determine a computer's HomeGroup membership status and display the sharing wizard.
helpviewer_keywords: ["IHomeGroup","IHomeGroup interface [Windows Shell]","IHomeGroup interface [Windows Shell]","described","_shell_IHomeGroup","shell.IHomeGroup","shobjidl_core/IHomeGroup"]
old-location: shell\IHomeGroup.htm
tech.root: shell
ms.assetid: 97d693c0-1126-4cd3-8aee-b5499b538403
ms.date: 12/05/2018
ms.keywords: IHomeGroup, IHomeGroup interface [Windows Shell], IHomeGroup interface [Windows Shell],described, _shell_IHomeGroup, shell.IHomeGroup, shobjidl_core/IHomeGroup
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.dll: Provsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IHomeGroup
 - shobjidl_core/IHomeGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Provsvc.dll
api_name:
 - IHomeGroup
---

# IHomeGroup interface


## -description

Exposes methods that determine a computer's HomeGroup membership status and display the sharing wizard.

## -inheritance

The <b>IHomeGroup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IHomeGroup</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Custom implementations of <b>IHomeGroup</b> are not supported; client applications use the implementation provided in Provsvc.dll.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use <b>IHomeGroup</b> when there is a need to determine the local computer's HomeGroup membership status; that is, to check wither the local computer is a member of a HomeGroup.



To create an instance of <b>IHomeGroup</b>, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> and specify <b>CLSID_HomeGroup</b> as the CLSID. <b>CLSID_HomeGroup</b> is defined in Shobjidl.h and Shobjidl.idl.
