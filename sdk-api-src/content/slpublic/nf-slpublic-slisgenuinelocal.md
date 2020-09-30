---
UID: NF:slpublic.SLIsGenuineLocal
title: SLIsGenuineLocal function (slpublic.h)
description: Checks whether the specified application is a genuine Windows installation.
helpviewer_keywords: ["SLIsGenuineLocal","SLIsGenuineLocal function [Security]","security.slisgenuinelocal","slpublic/SLIsGenuineLocal"]
old-location: security\slisgenuinelocal.htm
tech.root: security
ms.assetid: e1983777-13c1-4bf5-834d-471db3bfa0f6
ms.date: 12/05/2018
ms.keywords: SLIsGenuineLocal, SLIsGenuineLocal function [Security], security.slisgenuinelocal, slpublic/SLIsGenuineLocal
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Slwga.lib
req.dll: Slwga.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SLIsGenuineLocal
 - slpublic/SLIsGenuineLocal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slwga.dll
api_name:
 - SLIsGenuineLocal
---

# SLIsGenuineLocal function


## -description

Checks whether the specified application is a genuine Windows installation.

## -parameters

### -param pAppId [in]

A pointer to an <b>SLID</b> structure that specifies the application to check.

### -param pGenuineState [out]

A pointer to a value of the <a href="/windows/desktop/api/slpublic/ne-slpublic-sl_genuine_state">SL_GENUINE_STATE</a> enumeration that specifies the state of the installation.

### -param pUIOptions [in, out, optional]

A pointer to an <a href="/windows/desktop/api/slpublic/ns-slpublic-sl_nongenuine_ui_options">SL_NONGENUINE_UI_OPTIONS</a> structure that specifies a dialog box to display if the installation is not genuine. If the value of this parameter is <b>NULL</b>, no dialog box is displayed.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function checks the <b>Tampered</b> flag of the license associated with the specified application. If the license is not valid, or if the <b>Tampered</b> flag of the license is set, the installation is not considered valid.