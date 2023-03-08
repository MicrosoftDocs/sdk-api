---
UID: NN:gpedit.IGPEInformation
title: IGPEInformation (gpedit.h)
description: The IGPEInformation interface provides methods for Microsoft Management Console (MMC) extension snap-ins to communicate with the Group Policy Object Editor. For more information about MMC, see the Microsoft Management Console.
helpviewer_keywords: ["IGPEInformation","IGPEInformation interface [Group Policy]","IGPEInformation interface [Group Policy]","described","_win32_igpeinformation","gpedit/IGPEInformation","policy.igpeinformation"]
old-location: policy\igpeinformation.htm
tech.root: Policy
ms.assetid: 3b3e7793-fc69-43a3-a2b1-0aa36748a19b
ms.date: 12/05/2018
ms.keywords: IGPEInformation, IGPEInformation interface [Group Policy], IGPEInformation interface [Group Policy],described, _win32_igpeinformation, gpedit/IGPEInformation, policy.igpeinformation
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Gpedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPEInformation
 - gpedit/IGPEInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGPEInformation
---

# IGPEInformation interface


## -description

The
    <b>IGPEInformation</b> interface provides methods for Microsoft Management Console (MMC) extension snap-ins to communicate with the Group Policy Object Editor. For more information about MMC, see the 
<a href="/previous-versions/windows/desktop/mmc/mmc-programmer-s-guide">Microsoft Management Console</a>.

Note that this interface does not support multithreaded object concurrency.

## -inheritance

The <b>IGPEInformation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGPEInformation</b> also has these types of members:

## -remarks

To create and modify a GPO directly, without using the Group Policy Object Editor, see the methods of the 
<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>
