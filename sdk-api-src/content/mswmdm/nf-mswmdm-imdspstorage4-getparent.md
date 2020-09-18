---
UID: NF:mswmdm.IMDSPStorage4.GetParent
title: IMDSPStorage4::GetParent (mswmdm.h)
description: The GetParent method retrieves the parent of the current storage.
helpviewer_keywords: ["GetParent","GetParent method [windows Media Device Manager]","GetParent method [windows Media Device Manager]","IMDSPStorage4 interface","IMDSPStorage4 interface [windows Media Device Manager]","GetParent method","IMDSPStorage4.GetParent","IMDSPStorage4::GetParent","IMDSPStorage4GetParent","mswmdm/IMDSPStorage4::GetParent","wmdm.imdspstorage4_getparent"]
old-location: wmdm\imdspstorage4_getparent.htm
tech.root: WMDM
ms.assetid: 7b8264ef-9288-4196-9b92-a54a25aad795
ms.date: 12/05/2018
ms.keywords: GetParent, GetParent method [windows Media Device Manager], GetParent method [windows Media Device Manager],IMDSPStorage4 interface, IMDSPStorage4 interface [windows Media Device Manager],GetParent method, IMDSPStorage4.GetParent, IMDSPStorage4::GetParent, IMDSPStorage4GetParent, mswmdm/IMDSPStorage4::GetParent, wmdm.imdspstorage4_getparent
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDSPStorage4::GetParent
 - mswmdm/IMDSPStorage4::GetParent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPStorage4.GetParent
---

# IMDSPStorage4::GetParent


## -description

The <b>GetParent</b> method retrieves the parent of the current storage.

## -parameters

### -param ppStorage [out]

Pointer to the returned parent storage object.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method can be used to traverse the complete hierarchy of the current storage if used recursively.

When this method is called for root storage, this method should return S_FALSE and set <i>ppStorage</i> to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4">IMDSPStorage4 Interface</a>