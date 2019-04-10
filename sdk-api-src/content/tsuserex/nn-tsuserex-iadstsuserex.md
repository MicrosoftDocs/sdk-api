---
UID: NN:tsuserex.IADsTSUserEx
title: IADsTSUserEx (tsuserex.h)
author: windows-sdk-content
description: Used to examine and configure Remote Desktop Services user properties.
old-location: termserv\iadstsuserex.htm
tech.root: TermServ
ms.assetid: 7af8fe94-15db-49dc-ba4a-b79601205f59
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsTSUserEx, IADsTSUserEx interface [Remote Desktop Services], IADsTSUserEx interface [Remote Desktop Services],described, termserv.iadstsuserex, tsuserex/IADsTSUserEx
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tsuserex.dll
api_name:
 - IADsTSUserEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsTSUserEx interface


## -description


The property methods of the <b>IADsTSUserEx</b> interface can be used to examine 
   and configure Remote Desktop Services user properties. Properties include logon, <a href="https://msdn.microsoft.com/3993b664-82bb-4419-a06f-2a4e24003170">TerminalServicesHomeDirectory</a>, remote control, session, 
   and environment properties of the <b>IADsTSUserEx</b> class.

Before calling the methods of this interface, you must call the 
    <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a> method or the 
    <a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">IADs::GetInfoEx</a> method to load the property values of the 
    ADSI object from the underlying directory store into the property cache. Call 
    <b>IADs::GetInfo</b> to refresh all the property values for the 
    class; call <b>IADs::GetInfoEx</b> to refresh the values of 
    selected properties in the property cache.

After calling the methods of this interface, you must call the 
    <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a> method to save the property value changes in 
    the persistent store of the underlying directory store.

For more information, see <a href="https://msdn.microsoft.com/0d2b4117-11f2-4b39-8fe5-3b176e4256f4">The ADSI Attribute Cache</a> and the 
    reference section for the <a href="https://msdn.microsoft.com/8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd">ADSI Interfaces</a>. For a general discussion on 
    property methods, see <a href="https://msdn.microsoft.com/b2831fa4-b58d-4b65-8deb-5fb7cd50c724">Interface Property Methods</a>.

The following table lists the property methods of the <b>IADsTSUserEx</b> interface in 
    vtable order.


## -see-also




<a href="https://msdn.microsoft.com/8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd">ADSI Interfaces</a>



<a href="https://msdn.microsoft.com/df3b0a87-2a35-4cb9-9253-4695b5709318">Active Directory Service Interfaces Scripting</a>



<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>



<a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">IADs::GetInfoEx</a>



<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a>



<a href="https://msdn.microsoft.com/b2831fa4-b58d-4b65-8deb-5fb7cd50c724">Interface Property Methods</a>
 

 

