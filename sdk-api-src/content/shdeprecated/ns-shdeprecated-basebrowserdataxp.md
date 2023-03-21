---
UID: NS:shdeprecated.BASEBROWSERDATAXP
title: BASEBROWSERDATAXP (shdeprecated.h)
description: The BASEBROWSERDATAXP structure contains protected members of the base class. (BASEBROWSERDATAXP structure)
helpviewer_keywords: ["*LPBASEBROWSERDATA","*LPBASEBROWSERDATAXP","BASEBROWSERDATA","BASEBROWSERDATA structure [Windows Shell]","BASEBROWSERDATAXP","FALSE","LPCBASEBROWSERDATA","LPCBASEBROWSERDATA structure pointer [Windows Shell]","SECURELOCK_FIRSTSUGGEST","SECURELOCK_NOCHANGE","SECURELOCK_SET_FORTEZZA","SECURELOCK_SET_MIXED","SECURELOCK_SET_SECURE128BIT","SECURELOCK_SET_SECURE40BIT","SECURELOCK_SET_SECURE56BIT","SECURELOCK_SET_SECUREUNKNOWNBIT","SECURELOCK_SET_UNSECURE","SECURELOCK_SUGGEST_FORTEZZA","SECURELOCK_SUGGEST_MIXED","SECURELOCK_SUGGEST_SECURE128BIT","SECURELOCK_SUGGEST_SECURE40BIT","SECURELOCK_SUGGEST_SECURE56BIT","SECURELOCK_SUGGEST_SECUREUNKNOWNBIT","SECURELOCK_SUGGEST_UNSECURE","TRUE","shdeprecated/BASEBROWSERDATA","shdeprecated/LPCBASEBROWSERDATA","shell.BASEBROWSERDATA","zone_BASEBROWSERDATA"]
old-location: shell\BASEBROWSERDATA.htm
tech.root: shell
ms.assetid: d56e42e8-a556-4470-82d9-466edd84214f
ms.date: 08/02/2022
ms.keywords: '*LPBASEBROWSERDATA, *LPBASEBROWSERDATAXP, BASEBROWSERDATA, BASEBROWSERDATA structure [Windows Shell], BASEBROWSERDATAXP, FALSE, LPCBASEBROWSERDATA, LPCBASEBROWSERDATA structure pointer [Windows Shell], SECURELOCK_FIRSTSUGGEST, SECURELOCK_NOCHANGE, SECURELOCK_SET_FORTEZZA, SECURELOCK_SET_MIXED, SECURELOCK_SET_SECURE128BIT, SECURELOCK_SET_SECURE40BIT, SECURELOCK_SET_SECURE56BIT, SECURELOCK_SET_SECUREUNKNOWNBIT, SECURELOCK_SET_UNSECURE, SECURELOCK_SUGGEST_FORTEZZA, SECURELOCK_SUGGEST_MIXED, SECURELOCK_SUGGEST_SECURE128BIT, SECURELOCK_SUGGEST_SECURE40BIT, SECURELOCK_SUGGEST_SECURE56BIT, SECURELOCK_SUGGEST_SECUREUNKNOWNBIT, SECURELOCK_SUGGEST_UNSECURE, TRUE, shdeprecated/BASEBROWSERDATA, shdeprecated/LPCBASEBROWSERDATA, shell.BASEBROWSERDATA, zone_BASEBROWSERDATA'
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BASEBROWSERDATAXP, *LPBASEBROWSERDATAXP
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - BASEBROWSERDATAXP
 - shdeprecated/BASEBROWSERDATAXP
 - LPBASEBROWSERDATAXP
 - shdeprecated/LPBASEBROWSERDATAXP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shdeprecated.h
api_name:
 - BASEBROWSERDATA
---

# BASEBROWSERDATAXP structure


## -description

Contains protected members of the base class. <b>BASEBROWSERDATA</b> defines the browser state and is used with <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata">IBrowserService2::GetBaseBrowserData</a> and <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata">IBrowserService2::PutBaseBrowserData</a>.

## -struct-fields

### -field _hwnd

Type: <b>HWND</b>

The handle of the browser's top-level window.

### -field _ptl

Type: <b><a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-itravellog">ITravelLog</a>*</b>

A pointer to the browser's <a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-itravellog">ITravelLog</a>.

### -field _phlf

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)">IHlinkFrame</a>*</b>

A pointer to the browser's <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)">IHlinkFrame</a>.
    
                        

<div class="alert"><b>Note</b>  This member is only valid on first navigation from an hlink element-compatible application such as Word.</div>
<div> </div>

### -field _pautoWB2

Type: <b><a href="/windows/desktop/api/exdisp/nn-exdisp-iwebbrowser2">IWebBrowser2</a>*</b>

A pointer to the browser's <a href="/windows/desktop/api/exdisp/nn-exdisp-iwebbrowser2">IWebBrowser2</a> object.

### -field _pautoEDS

Type: <b><a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-iexpdispsupport">IExpDispSupport</a>*</b>

A pointer to the browser's <a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-iexpdispsupport">IExpDispSupport</a> object.

### -field _pautoSS

Type: <b><a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-ishellservice">IShellService</a>*</b>

A pointer to the browser's <a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-ishellservice">IShellService</a> object.

### -field _eSecureLockIcon

Type: <b>int</b>

One of the following values to indicate the security lock icon.



#### SECURELOCK_NOCHANGE (-1)

No change in security encryption status.



#### SECURELOCK_SET_UNSECURE (0)

Default. 0x0000. No security encryption present.



#### SECURELOCK_SET_MIXED

There are multiple security encryption methods present.



#### SECURELOCK_SET_SECUREUNKNOWNBIT

The security encryption level is not known.



#### SECURELOCK_SET_SECURE40BIT

There is 40-bit security encryption present.



#### SECURELOCK_SET_SECURE56BIT

There is 56-bit security encryption present.



#### SECURELOCK_SET_FORTEZZA

There is Fortezza security encryption present.



#### SECURELOCK_SET_SECURE128BIT

There is 128-bit security encryption present.



#### SECURELOCK_FIRSTSUGGEST

A security encryption setting should be suggested.



#### SECURELOCK_SUGGEST_UNSECURE (SECURELOCK_FIRSTSUGGEST)

No security encryption has been suggested.



#### SECURELOCK_SUGGEST_MIXED

Mixed security encryption methods have been suggested.



#### SECURELOCK_SUGGEST_SECUREUNKNOWNBIT

Unknown security encryption method has been suggested.



#### SECURELOCK_SUGGEST_SECURE40BIT

40-bit security encryption has been suggested.



#### SECURELOCK_SUGGEST_SECURE56BIT

56-bit security encryption has been suggested.



#### SECURELOCK_SUGGEST_FORTEZZA

Fortezza security encryption has been suggested.



#### SECURELOCK_SUGGEST_SECURE128BIT

128-bit security encryption has been suggested.

### -field _fCreatingViewWindow

Type: <b>UINT</b>

A view window is being created by the browser.

### -field _uActivateState

Type: <b>UINT</b>

The browser view is in an activated state.

### -field _pidlViewState

### -field _pctView

Type: <b><a href="/windows/desktop/api/docobj/nn-docobj-iolecommandtarget">IOleCommandTarget</a>*</b>

A cached pointer to the <a href="/windows/desktop/api/docobj/nn-docobj-iolecommandtarget">IOleCommandTarget</a> object associated with the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object pointed to by <b>_psv</b>.

### -field _pidlCur

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL of the current navigated location of the browser. This value is the same retrieved by <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-getpidl">IBrowserService::GetPidl</a>.

### -field _psv

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> of the current location. This <b>IShellView</b> is bound to <b>_pidlCur</b> through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject">IShellFolder::CreateViewObject</a>.

### -field _psf

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> of the current location. This <b>IShellFolder</b> is bound to <b>_pidlCur</b>.

### -field _hwndView

Type: <b>HWND</b>

A handle to the window returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow">_psv->CreateViewWindow</a>.

### -field _pszTitleCur

Type: <b>LPWSTR</b>

A pointer to a buffer containing the Unicode title text for the current location.

### -field _pidlPending

Type: <b>PCIDLIST_ABSOLUTE</b>

The PIDL of the pending target location. Once navigation is complete, this value moves to <b>_pidlCur</b>.

### -field _psvPending

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> of the pending target location. Once navigation is complete, this value moves to <b>_psv</b>.

### -field _psfPending

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> of the pending target location. Once navigation is complete, this value moves to <b>_psf</b>.

### -field _hwndViewPending

Type: <b>HWND</b>

A handle to the pending target location's view window. Once navigation is complete, this value moves to <b>_hwndView</b>.

### -field _pszTitlePending

Type: <b>LPWSTR</b>

A pointer to a buffer containing the Unicode title text for the pending target location. Once navigation is complete, this value moves to <b>_pszTitleCur</b>.

### -field _fIsViewMSHTML

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates whether the browser is hosting folder content or web content.



#### TRUE

The browser is hosting web content.



#### FALSE

The browser is hosting folder content.

### -field _fPrivacyImpacted

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates whether there is a privacy concern with the browser's content.



#### TRUE

There is a privacy concern with the browser's content.



#### FALSE

There is not a privacy concern with the browser's content.

### -field _clsidView

Type: <b>CLSID</b>

### -field _clsidViewPending

Type: <b>CLSID</b>

### -field _hwndFrame

Type: <b>HWND</b>

### -field _eSecureLockIcon.SECURELOCK_FIRSTSUGGEST

A security encryption setting should be suggested.

### -field _eSecureLockIcon.SECURELOCK_NOCHANGE (-1)

No change in security encryption status.

### -field _eSecureLockIcon.SECURELOCK_SET_FORTEZZA

There is Fortezza security encryption present.

### -field _eSecureLockIcon.SECURELOCK_SET_MIXED

There are multiple security encryption methods present.

### -field _eSecureLockIcon.SECURELOCK_SET_SECURE128BIT

There is 128-bit security encryption present.

### -field _eSecureLockIcon.SECURELOCK_SET_SECURE40BIT

There is 40-bit security encryption present.

### -field _eSecureLockIcon.SECURELOCK_SET_SECURE56BIT

There is 56-bit security encryption present.

### -field _eSecureLockIcon.SECURELOCK_SET_SECUREUNKNOWNBIT

The security encryption level is not known.

### -field _eSecureLockIcon.SECURELOCK_SET_UNSECURE (0)

Default. 0x0000. No security encryption present.

### -field _eSecureLockIcon.SECURELOCK_SUGGEST_FORTEZZA

Fortezza security encryption has been suggested.

### -field _eSecureLockIcon.SECURELOCK_SUGGEST_MIXED

Mixed security encryption methods have been suggested.

### -field _eSecureLockIcon.SECURELOCK_SUGGEST_SECURE128BIT

128-bit security encryption has been suggested.

### -field _eSecureLockIcon.SECURELOCK_SUGGEST_SECURE40BIT

40-bit security encryption has been suggested.

### -field _eSecureLockIcon.SECURELOCK_SUGGEST_SECURE56BIT

56-bit security encryption has been suggested.

### -field _eSecureLockIcon.SECURELOCK_SUGGEST_SECUREUNKNOWNBIT

Unknown security encryption method has been suggested.

### -field _eSecureLockIcon.SECURELOCK_SUGGEST_UNSECURE (SECURELOCK_FIRSTSUGGEST)

No security encryption has been suggested.

### -field _fIsViewMSHTML.FALSE

The browser is hosting folder content.

### -field _fIsViewMSHTML.TRUE

The browser is hosting web content.

### -field _fPrivacyImpacted.FALSE

There is not a privacy concern with the browser's content.

### -field _fPrivacyImpacted.TRUE

There is a privacy concern with the browser's content.


#### - _lPhishingFilterStatus

Type: <b>LONG</b>

<b>Windows Vista with Service Pack 1 (SP1) and later or Windows Internet Explorer 7 and later only</b>. 0 if the phishing filter is off; 1 if it is on.


#### - _pidlNewShellView

Type: <b>PCIDLIST_ABSOLUTE</b>

A temporary placeholder for <b>_pidlPending</b> on first navigation to the pending location.
