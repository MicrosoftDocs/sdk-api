---
UID: NN:tsuserex.IADsTSUserEx
title: IADsTSUserEx (tsuserex.h)
description: Used to examine and configure Remote Desktop Services user properties.
helpviewer_keywords: ["IADsTSUserEx","IADsTSUserEx interface [Remote Desktop Services]","IADsTSUserEx interface [Remote Desktop Services]","described","termserv.iadstsuserex","tsuserex/IADsTSUserEx"]
old-location: termserv\iadstsuserex.htm
tech.root: TermServ
ms.assetid: 7af8fe94-15db-49dc-ba4a-b79601205f59
ms.date: 12/05/2018
ms.keywords: IADsTSUserEx, IADsTSUserEx interface [Remote Desktop Services], IADsTSUserEx interface [Remote Desktop Services],described, termserv.iadstsuserex, tsuserex/IADsTSUserEx
req.header: tsuserex.h
req.include-header: Tsuserex.h, Tsuserex_i.c
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
req.type-library: Tsuserex.tlb
req.lib: 
req.dll: Tsuserex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsTSUserEx
 - tsuserex/IADsTSUserEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tsuserex.dll
api_name:
 - IADsTSUserEx
---

# IADsTSUserEx interface


## -description

The property methods of the <b>IADsTSUserEx</b> interface can be used to examine 
   and configure Remote Desktop Services user properties. Properties include logon, <a href="/windows/desktop/api/tsuserex/nf-tsuserex-iadstsuserex-get_terminalserviceshomedirectory">TerminalServicesHomeDirectory</a>, remote control, session, 
   and environment properties of the <b>IADsTSUserEx</b> class.

Before calling the methods of this interface, you must call the 
    <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a> method or the 
    <a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a> method to load the property values of the 
    ADSI object from the underlying directory store into the property cache. Call 
    <b>IADs::GetInfo</b> to refresh all the property values for the 
    class; call <b>IADs::GetInfoEx</b> to refresh the values of 
    selected properties in the property cache.

After calling the methods of this interface, you must call the 
    <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a> method to save the property value changes in 
    the persistent store of the underlying directory store.

For more information, see <a href="/windows/desktop/ADSI/the-adsi-attribute-cache">The ADSI Attribute Cache</a> and the 
    reference section for the <a href="/windows/desktop/ADSI/adsi-interfaces">ADSI Interfaces</a>. For a general discussion on 
    property methods, see <a href="/windows/desktop/ADSI/interface-property-methods">Interface Property Methods</a>.

The following table lists the property methods of the <b>IADsTSUserEx</b> interface in 
    vtable order.

## -see-also

<a href="/windows/desktop/ADSI/adsi-interfaces">ADSI Interfaces</a>



<a href="/windows/desktop/ADSI/adsi-scripting-tutorial">Active Directory Service Interfaces Scripting</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a>



<a href="/windows/desktop/ADSI/interface-property-methods">Interface Property Methods</a>