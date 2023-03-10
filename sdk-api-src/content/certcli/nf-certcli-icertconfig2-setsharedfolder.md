---
UID: NF:certcli.ICertConfig2.SetSharedFolder
title: ICertConfig2::SetSharedFolder (certcli.h)
description: Specifies the path to be used as the certification authority's (CA) shared folder.
helpviewer_keywords: ["CCertConfig object [Security]","SetSharedFolder method","ICertConfig2 interface [Security]","SetSharedFolder method","ICertConfig2.SetSharedFolder","ICertConfig2::SetSharedFolder","SetSharedFolder","SetSharedFolder method [Security]","SetSharedFolder method [Security]","CCertConfig object","SetSharedFolder method [Security]","ICertConfig2 interface","_certsrv_icertconfig2_setsharedfolder","certcli/ICertConfig2::SetSharedFolder","security.icertconfig2_setsharedfolder"]
old-location: security\icertconfig2_setsharedfolder.htm
tech.root: security
ms.assetid: f0fc4218-ca07-4488-bd0c-bfa8bdcd2179
ms.date: 12/05/2018
ms.keywords: CCertConfig object [Security],SetSharedFolder method, ICertConfig2 interface [Security],SetSharedFolder method, ICertConfig2.SetSharedFolder, ICertConfig2::SetSharedFolder, SetSharedFolder, SetSharedFolder method [Security], SetSharedFolder method [Security],CCertConfig object, SetSharedFolder method [Security],ICertConfig2 interface, _certsrv_icertconfig2_setsharedfolder, certcli/ICertConfig2::SetSharedFolder, security.icertconfig2_setsharedfolder
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertConfig2::SetSharedFolder
 - certcli/ICertConfig2::SetSharedFolder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertConfig2.SetSharedFolder
 - CCertConfig.SetSharedFolder
---

# ICertConfig2::SetSharedFolder


## -description

The <b>SetSharedFolder</b> method specifies the path to be used as the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>'s (CA) shared folder. This method was first defined in the <a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a> interface.

## -parameters

### -param strSharedFolder [in]

String value that specifies the path of the new shared folder directory.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.