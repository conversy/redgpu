Oct 09, 2021:

  * REDGPU log debug libraries are added, they redirect the console debug print output to /tmp/redgpu.txt file on Linux and redgpu.txt file located in executable's folder on Windows.
  * REDGPU debug library: context pointers are now printed as well.

Oct 07, 2021:

  * libredgpu.so is now compiled with Clang 13.
  * libredgpu.so.su static stack usage analysis file is added, it specifies the maximum amount of stack used per procedure, in bytes. (Not relevant to the public API: internally, PPHI stands for Procedure Parameters Handles Implementation.)
  * Fixed a bug when procedures could return empty RedStatuses::statusErrorDescription strings for some errors.
  * The stack size of internal statuses setting procedures is minimized.

Oct 03, 2021:

  * **NEW**: `redgpu_array_timestamp.h` extension.
  * REDGPU debug library: RedStatuses::statusFile and RedStatuses::statusErrorFile strings are now printed in quotes.

Sep 19, 2021:

  * **NEW**: `redgpu_context_from_vk.h::RedContextOptionalSettingsContextFromVkGetInstanceProcAddr` struct.

Sep 07, 2021:

  * **NEW**: `redgpu_computing_language.h` extension.
  * **NEW**: `redgpu_context_from_vk.h` context optional settings.
  * Minor improvement to internal GPU statuses setting of redCreateContext.
  * Status code info strings are now set to RedStatuses::statusErrorDescription.

Aug 25, 2021:

  * Fix redCreatePresent::outStatuses setting that could incorrectly set ::statusProcedureId and ::statusErrorProcedureId to RED_PROCEDURE_ID_redQueuePresent.
  * Internal statuses setting optimizations.

Aug 11, 2021:

  * Release REDGPU under Apache License, Version 2.0.
