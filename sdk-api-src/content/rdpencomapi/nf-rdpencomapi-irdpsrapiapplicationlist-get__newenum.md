---
UID: NF:rdpencomapi.IRDPSRAPIApplicationList.get__NewEnum
title: IRDPSRAPIApplicationList::get__NewEnum (rdpencomapi.h)
description: An enumerator interface for the application collection.
helpviewer_keywords: ["IRDPSRAPIApplicationList interface [RDP]","_NewEnum property","IRDPSRAPIApplicationList._NewEnum","IRDPSRAPIApplicationList.get__NewEnum","IRDPSRAPIApplicationList::_NewEnum","IRDPSRAPIApplicationList::get__NewEnum","RDPSRAPIApplicationList object [RDP]","_NewEnum property","_NewEnum property [RDP]","_NewEnum property [RDP]","IRDPSRAPIApplicationList interface","_NewEnum property [RDP]","RDPSRAPIApplicationList object","get__NewEnum","rdp.irdpsrapiapplicationlist__newenum","rdpencomapi/IRDPSRAPIApplicationList::_NewEnum","rdpencomapi/IRDPSRAPIApplicationList::get__NewEnum"]
old-location: rdp\irdpsrapiapplicationlist__newenum.htm
tech.root: rdp
ms.assetid: 946cba06-9cc1-4a44-aeed-0b636d737edd
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIApplicationList interface [RDP],_NewEnum property, IRDPSRAPIApplicationList._NewEnum, IRDPSRAPIApplicationList.get__NewEnum, IRDPSRAPIApplicationList::_NewEnum, IRDPSRAPIApplicationList::get__NewEnum, RDPSRAPIApplicationList object [RDP],_NewEnum property, _NewEnum property [RDP], _NewEnum property [RDP],IRDPSRAPIApplicationList interface, _NewEnum property [RDP],RDPSRAPIApplicationList object, get__NewEnum, rdp.irdpsrapiapplicationlist__newenum, rdpencomapi/IRDPSRAPIApplicationList::_NewEnum, rdpencomapi/IRDPSRAPIApplicationList::get__NewEnum
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPIApplicationList::get__NewEnum
 - rdpencomapi/IRDPSRAPIApplicationList::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIApplicationList._NewEnum
 - IRDPSRAPIApplicationList.get__NewEnum
 - RDPSRAPIApplicationList._NewEnum
---

# IRDPSRAPIApplicationList::get__NewEnum


## -description

An enumerator interface for the application collection.

This property is read-only.

## -parameters

## -remarks

The enumerator provides a snapshot of the collection. If an application is destroyed during enumeration, the API still has access to all the elements that were present when the snapshot was taken.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiapplicationlist">IRDPSRAPIApplicationList</a>