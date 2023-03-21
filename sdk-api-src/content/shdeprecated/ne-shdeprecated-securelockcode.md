---
UID: NE:shdeprecated.SECURELOCKCODE
title: SECURELOCKCODE (shdeprecated.h)
description: Deprecated. This enumeration is used by the BASEBROWSERDATA structure to indicate the base browser's lock icon status.
helpviewer_keywords: ["SECURELOCK","SECURELOCK enumeration [Windows Shell]","SECURELOCKCODE","SECURELOCK_FIRSTSUGGEST","SECURELOCK_NOCHANGE","SECURELOCK_SET_FORTEZZA","SECURELOCK_SET_MIXED","SECURELOCK_SET_SECURE128BIT","SECURELOCK_SET_SECURE40BIT","SECURELOCK_SET_SECURE56BIT","SECURELOCK_SET_SECUREUNKNOWNBIT","SECURELOCK_SET_UNSECURE","SECURELOCK_SUGGEST_FORTEZZA","SECURELOCK_SUGGEST_MIXED","SECURELOCK_SUGGEST_SECURE128BIT","SECURELOCK_SUGGEST_SECURE40BIT","SECURELOCK_SUGGEST_SECURE56BIT","SECURELOCK_SUGGEST_SECUREUNKNOWNBIT","SECURELOCK_SUGGEST_UNSECURE","_win32_SECURELOCK","shdeprecated/SECURELOCK","shdeprecated/SECURELOCK_FIRSTSUGGEST","shdeprecated/SECURELOCK_NOCHANGE","shdeprecated/SECURELOCK_SET_FORTEZZA","shdeprecated/SECURELOCK_SET_MIXED","shdeprecated/SECURELOCK_SET_SECURE128BIT","shdeprecated/SECURELOCK_SET_SECURE40BIT","shdeprecated/SECURELOCK_SET_SECURE56BIT","shdeprecated/SECURELOCK_SET_SECUREUNKNOWNBIT","shdeprecated/SECURELOCK_SET_UNSECURE","shdeprecated/SECURELOCK_SUGGEST_FORTEZZA","shdeprecated/SECURELOCK_SUGGEST_MIXED","shdeprecated/SECURELOCK_SUGGEST_SECURE128BIT","shdeprecated/SECURELOCK_SUGGEST_SECURE40BIT","shdeprecated/SECURELOCK_SUGGEST_SECURE56BIT","shdeprecated/SECURELOCK_SUGGEST_SECUREUNKNOWNBIT","shdeprecated/SECURELOCK_SUGGEST_UNSECURE","shell.SECURELOCK"]
old-location: shell\SECURELOCK.htm
tech.root: shell
ms.assetid: 36426bd3-d7c3-4636-99d6-2177f0b7fe3f
ms.date: 12/05/2018
ms.keywords: SECURELOCK, SECURELOCK enumeration [Windows Shell], SECURELOCKCODE, SECURELOCK_FIRSTSUGGEST, SECURELOCK_NOCHANGE, SECURELOCK_SET_FORTEZZA, SECURELOCK_SET_MIXED, SECURELOCK_SET_SECURE128BIT, SECURELOCK_SET_SECURE40BIT, SECURELOCK_SET_SECURE56BIT, SECURELOCK_SET_SECUREUNKNOWNBIT, SECURELOCK_SET_UNSECURE, SECURELOCK_SUGGEST_FORTEZZA, SECURELOCK_SUGGEST_MIXED, SECURELOCK_SUGGEST_SECURE128BIT, SECURELOCK_SUGGEST_SECURE40BIT, SECURELOCK_SUGGEST_SECURE56BIT, SECURELOCK_SUGGEST_SECUREUNKNOWNBIT, SECURELOCK_SUGGEST_UNSECURE, _win32_SECURELOCK, shdeprecated/SECURELOCK, shdeprecated/SECURELOCK_FIRSTSUGGEST, shdeprecated/SECURELOCK_NOCHANGE, shdeprecated/SECURELOCK_SET_FORTEZZA, shdeprecated/SECURELOCK_SET_MIXED, shdeprecated/SECURELOCK_SET_SECURE128BIT, shdeprecated/SECURELOCK_SET_SECURE40BIT, shdeprecated/SECURELOCK_SET_SECURE56BIT, shdeprecated/SECURELOCK_SET_SECUREUNKNOWNBIT, shdeprecated/SECURELOCK_SET_UNSECURE, shdeprecated/SECURELOCK_SUGGEST_FORTEZZA, shdeprecated/SECURELOCK_SUGGEST_MIXED, shdeprecated/SECURELOCK_SUGGEST_SECURE128BIT, shdeprecated/SECURELOCK_SUGGEST_SECURE40BIT, shdeprecated/SECURELOCK_SUGGEST_SECURE56BIT, shdeprecated/SECURELOCK_SUGGEST_SECUREUNKNOWNBIT, shdeprecated/SECURELOCK_SUGGEST_UNSECURE, shell.SECURELOCK
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - SECURELOCKCODE
 - shdeprecated/SECURELOCKCODE
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
 - SECURELOCK
---

# SECURELOCKCODE enumeration


## -description

Deprecated. This enumeration is used by the <a href="/windows/desktop/api/shdeprecated/ns-shdeprecated-basebrowserdatalh">BASEBROWSERDATA</a> structure to indicate the base browser's lock icon status.

## -enum-fields

### -field SECURELOCK_NOCHANGE:-1

No change in security encryption status.

### -field SECURELOCK_SET_UNSECURE:0

There is no security encryption present.

### -field SECURELOCK_SET_MIXED

There are multiple security encryption methods present.

### -field SECURELOCK_SET_SECUREUNKNOWNBIT

The security encryption level is not known.

### -field SECURELOCK_SET_SECURE40BIT

There is 40-bit security encryption present.

### -field SECURELOCK_SET_SECURE56BIT

There is 56-bit security encryption present.

### -field SECURELOCK_SET_FORTEZZA

There is Fortezza security encryption present.

### -field SECURELOCK_SET_SECURE128BIT

There is 128-bit security encryption present.

### -field SECURELOCK_FIRSTSUGGEST

Suggest a security encryption setting.

### -field SECURELOCK_SUGGEST_UNSECURE

No security encryption has been suggested.

### -field SECURELOCK_SUGGEST_MIXED

Mixed security encryption methods have been suggested.

### -field SECURELOCK_SUGGEST_SECUREUNKNOWNBIT

An unknown security encryption method has been suggested.

### -field SECURELOCK_SUGGEST_SECURE40BIT

A 40-bit security encryption has been suggested.

### -field SECURELOCK_SUGGEST_SECURE56BIT

A 56-bit security encryption has been suggested.

### -field SECURELOCK_SUGGEST_FORTEZZA

A Fortezza security encryption has been suggested.

### -field SECURELOCK_SUGGEST_SECURE128BIT

A 128-bit security encryption has been suggested.
