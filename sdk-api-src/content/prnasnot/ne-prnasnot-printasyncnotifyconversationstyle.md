---
UID: NE:prnasnot.PrintAsyncNotifyConversationStyle
title: PrintAsyncNotifyConversationStyle (prnasnot.h)
description: Specifies whether communication is bidirectional or unidirectional between applications and Print Spooler-hosted components such as printer drivers, print processors, and port monitors.
helpviewer_keywords: ["PrintAsyncNotifyConversationStyle","PrintAsyncNotifyConversationStyle enumeration [Windows GDI]","_win32_PrintAsyncNotifyConversationStyle","gdi.printasyncnotifyconversationstyle","kBiDirectional","kUniDirectional","prnasnot/PrintAsyncNotifyConversationStyle","prnasnot/kBiDirectional","prnasnot/kUniDirectional"]
old-location: gdi\printasyncnotifyconversationstyle.htm
tech.root: xps
ms.assetid: 61fefc3b-7299-4b52-962d-98f4c2f386dc
ms.date: 12/05/2018
ms.keywords: PrintAsyncNotifyConversationStyle, PrintAsyncNotifyConversationStyle enumeration [Windows GDI], _win32_PrintAsyncNotifyConversationStyle, gdi.printasyncnotifyconversationstyle, kBiDirectional, kUniDirectional, prnasnot/PrintAsyncNotifyConversationStyle, prnasnot/kBiDirectional, prnasnot/kUniDirectional
req.header: prnasnot.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PrintAsyncNotifyConversationStyle
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PrintAsyncNotifyConversationStyle
 - prnasnot/PrintAsyncNotifyConversationStyle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - prnasnot.h
api_name:
 - PrintAsyncNotifyConversationStyle
---

# PrintAsyncNotifyConversationStyle enumeration


## -description

Specifies whether communication is bidirectional or unidirectional between applications and Print Spooler-hosted components such as printer drivers, print processors, and port monitors.

## -enum-fields

### -field kBiDirectional

Indicates that applications can send replies to the Print Spooler-hosted component that sent a notification.

### -field kUniDirectional

Indicates that communication goes only from the Print Spooler-hosted component to one or more listening applications.

## -remarks

Even when the communication is bidirectional, applications cannot initiate communication. They can only reply to notifications sent by the Print Spooler-hosted components.

When multiple applications listen for bidirectional notifications, they receive only the first notification sent through a bidirectional channel. The Print Spooler maintains the channel only with the first listening application that responded, and discards all subsequent replies from other listeners.

